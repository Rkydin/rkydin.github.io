---
title: "Desktop Face Recognition Tool"
excerpt: "Python application using OpenCV and face_recognition library with a Tkinter UI for enrolling and recognizing users from a webcam stream."
date: 2025-05-01
header:
  teaser: /images/face-recognition/main-menu.png
collection: portfolio
---

## Project Overview

Developed a desktop face recognition application in Python that can enroll new users and recognize them in real-time from a webcam stream. The application uses OpenCV for video capture and the face_recognition library to identify individuals. Face encodings are stored as pickle files for persistent recognition across sessions.

## Project Gallery

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 30px 0;">
  <div>
    <img src="/images/face-recognition/main-menu.png" alt="Main menu" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Face Recognition System main menu</em></p>
  </div>
  <div>
    <img src="/images/face-recognition/name-entry.png" alt="Name entry" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Enter person's name before enrollment</em></p>
  </div>
  <div>
    <img src="/images/face-recognition/face-capture.png" alt="Face capture" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Face positioning and capture interface</em></p>
  </div>
  <div>
    <img src="/images/face-recognition/registered-faces.png" alt="Registered faces" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>View and manage enrolled faces</em></p>
  </div>
  <div>
    <img src="/images/face-recognition/delete-confirmation.png" alt="Delete confirmation" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Confirmation popup when deleting</em></p>
  </div>
  <div>
    <img src="/images/face-recognition/recognition-demo-1.png" alt="Recognition demo 1" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Real-time recognition with confidence scores</em></p>
  </div>
  <div>
    <img src="/images/face-recognition/recognition-demo-2.png" alt="Recognition demo 2" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Multi-face detection and recognition</em></p>
  </div>
</div>

## Key Features

* **Real-time face detection and recognition** from webcam feed with confidence scores
* **User enrollment system** that saves face encodings to disk
* **Face database management** - view, add, and delete registered faces
* **Automatic package installation system** for dependencies
* **Persistent storage** using pickle files
* **Multi-face detection** - recognizes multiple people simultaneously
* **FPS counter** for performance monitoring
* **Intuitive GUI** with clear instructions

## Technologies Used

* **Python** - Core programming language
* **OpenCV (cv2)** - Video capture and image processing
* **face_recognition library** - Face detection and encoding
* **Tkinter** - GUI framework for dialogs and interface
* **pickle** - Serialization for saving face encodings
* **NumPy** - Array operations

## System Interface

![Main Menu](/images/face-recognition/main-menu.png)
*Clean main menu with three primary functions: recognize faces, register new faces, and view registered faces*

## How It Works

The application captures frames from the webcam in real-time, detects faces in each frame, and compares them against a database of stored face encodings saved as `.pkl` files.

### System Features
- **Auto-installer**: Automatically detects and installs missing packages (face_recognition, opencv-python, numpy)
- **Camera initialization**: Robust camera setup with error handling and verification
- **Face database**: Stores face encodings in `known_faces/` directory as pickle files
- **Performance metrics**: Real-time FPS display

### Enrollment Process

![Name Entry](/images/face-recognition/name-entry.png)
*Enter the person's name before capturing their face*

![Face Capture](/images/face-recognition/face-capture.png)
*Position face within the oval guide and press SPACE to capture*

1. User selects "Register New Face"
2. Enter person's name
3. Position face within the oval guide
4. Press SPACE to capture multiple angles
5. Face encoding is generated and saved as `{name}.pkl`
6. Person is now in the recognition database

### Face Database Management

![Registered Faces](/images/face-recognition/registered-faces.png)
*View all enrolled faces with de
