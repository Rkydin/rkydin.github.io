---
title: "Desktop Face Recognition Tool"
excerpt: "Python application using OpenCV and face_recognition library with a Tkinter UI for enrolling and recognizing users from a webcam stream."
date: 2025-05-01
header:
  teaser: /images/face-recognition/main-menu.png
gallery:
  - url: /images/face-recognition/main-menu.png
    image_path: /images/face-recognition/main-menu.png
    alt: "Main menu interface"
    title: "Face Recognition System main menu"
  - url: /images/face-recognition/name-entry.png
    image_path: /images/face-recognition/name-entry.png
    alt: "Name entry screen"
    title: "Enter person's name before enrollment"
  - url: /images/face-recognition/face-capture.png
    image_path: /images/face-recognition/face-capture.png
    alt: "Face capture in progress"
    title: "Face positioning and capture interface"
  - url: /images/face-recognition/registered-faces.png
    image_path: /images/face-recognition/registered-faces.png
    alt: "Registered faces database"
    title: "View and manage enrolled faces"
  - url: /images/face-recognition/delete-confirmation.png
    image_path: /images/face-recognition/delete-confirmation.png
    alt: "Delete confirmation dialog"
    title: "Confirmation popup when deleting a registered face"
  - url: /images/face-recognition/recognition-demo-1.png
    image_path: /images/face-recognition/recognition-demo-1.png
    alt: "Recognition demo with Elon and Trump"
    title: "Real-time face recognition with confidence scores"
  - url: /images/face-recognition/recognition-demo-2.png
    image_path: /images/face-recognition/recognition-demo-2.png
    alt: "Recognition demo with Anne and Keanu"
    title: "Multi-face detection and recognition"
collection: portfolio
---

## Project Overview

Developed a desktop face recognition application in Python that can enroll new users and recognize them in real-time from a webcam stream. The application uses OpenCV for video capture and the face_recognition library to identify individuals. Face encodings are stored as pickle files for persistent recognition across sessions.

## Project Gallery

{% include gallery caption="Face Recognition System Interface and Demo" %}

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
*View all enrolled faces with delete options and add from file capability*

The system provides a complete face management interface where you can:
- View all registered faces
- Delete faces with confirmation dialog
- Add faces from image files
- Navigate through pages if many faces are registered

![Delete Confirmation](/images/face-recognition/delete-confirmation.png)
*Safety confirmation before deleting a registered face*

### Recognition in Action

![Recognition Demo 1](/images/face-recognition/recognition-demo-1.png)
*Real-time recognition with confidence percentages and FPS counter*

![Recognition Demo 2](/images/face-recognition/recognition-demo-2.png)
*System successfully detects and recognizes multiple faces simultaneously*

The recognition system:
1. Loads all known face encodings from disk on startup
2. Captures live video stream from webcam
3. Detects all faces in each frame
4. Compares face encodings against known faces database
5. Displays names with confidence percentages
6. Shows real-time FPS performance

## Technical Implementation

**Face Storage System:**
- Face encodings stored in: `known_faces/` directory
- Each person's encoding saved as `{name}.pkl`
- Persistent storage across program sessions
- Add faces from existing image files

**Performance:**
- Real-time processing at ~15 FPS
- Efficient face encoding comparison
- Multi-face detection capability
- Confidence scoring for matches

**Error Handling:**
- Automatic package installation on first run
- Camera initialization verification
- Graceful error messages for troubleshooting
- Confirmation dialogs for destructive actions

## Challenges & Solutions

**Challenge:** Ensuring all required packages are installed  
**Solution:** Implemented automatic package detection and installation system that checks for missing dependencies and installs them using pip

**Challenge:** Creating an intuitive user interface  
**Solution:** Designed a clean menu system with clear instructions and visual guides (like the oval face positioning guide)

**Challenge:** Managing face database efficiently  
**Solution:** Used pickle serialization for fast save/load operations and created a dedicated management interface

**Challenge:** Maintaining good performance with real-time recognition  
**Solution:** Optimized face detection and encoding comparison, achieving ~15 FPS with multiple faces

## Results

Successfully created a fully-featured face recognition system that:
- ✅ Automatically handles dependency installation
- ✅ Provides complete face enrollment and management
- ✅ Recognizes multiple faces simultaneously in real-time
- ✅ Shows confidence scores for recognition accuracy
- ✅ Maintains persistent face database across sessions
- ✅ Offers intuitive GUI for all operations
- ✅ Performs at real-time speeds (~15 FPS)

## Skills Demonstrated

* Python file I/O and serialization
* Computer vision with OpenCV
* Face recognition algorithms
* GUI design and user experience
* Error handling and validation
* Performance optimization
* Package management and dependencies
* Real-time video processing

## Future Improvements

* Add training mode with multiple face angles
* Implement adjustable confidence thresholds
* Add face anti-spoofing features
* Export/import face databases
* Add facial expression recognition
* Support for multiple camera sources
* Enhanced GUI with more customization options
* Add logging and usage statistics
