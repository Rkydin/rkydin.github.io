---
title: "Desktop Face Recognition Tool"
excerpt: "Python application using OpenCV and face_recognition library with a Tkinter UI for enrolling and recognizing users from a webcam stream."
date: 2025-05-01
header:
  teaser: /images/face-recognition.jpg
collection: portfolio
---

## Project Overview

Developed a desktop face recognition application in Python that can enroll new users and recognize them in real-time from a webcam stream. The application uses OpenCV for video capture and the face_recognition library to identify individuals. Face encodings are stored as pickle files for persistent recognition across sessions.

## Key Features

* Real-time face detection and recognition from webcam feed
* User enrollment system that saves face encodings to disk
* Automatic package installation system
* Persistent face database using pickle files
* Camera initialization with error handling
* Simple Tkinter-based interface

## Technologies Used

* **Python** - Core programming language
* **OpenCV (cv2)** - Video capture and image processing
* **face_recognition library** - Face detection and encoding
* **Tkinter** - GUI framework for file dialogs
* **pickle** - Serialization for saving face encodings
* **NumPy** - Array operations

## How It Works

The application captures frames from the webcam in real-time, detects faces in each frame, and compares them against a database of stored face encodings saved as `.pkl` files.

### System Features
- **Auto-installer**: Automatically detects and installs missing packages (face_recognition, opencv-python, numpy)
- **Camera initialization**: Robust camera setup with error handling and verification
- **Face database**: Stores face encodings in `known_faces/` directory as pickle files

### Enrollment Process
1. Capture face from webcam
2. Generate face encoding
3. Save encoding with person's name as a `.pkl` file
4. Face is now in the recognition database

### Recognition Process
1. Load all known face encodings from disk on startup
2. Capture live video stream from webcam
3. Detect faces in each frame
4. Compare face encodings against known faces database
5. Display recognition results

## Technical Implementation

**Face Storage System:**
- Face encodings stored in: `E:\Python Projects\FacialRecognition\known_faces\`
- Each person's encoding saved as `{name}.pkl`
- Persistent storage across program sessions

**Error Handling:**
- Automatic package installation on first run
- Camera initialization verification
- Graceful error messages for troubleshooting

## Challenges & Solutions

**Challenge:** Ensuring all required packages are installed  
**Solution:** Implemented automatic package detection and installation system that checks for missing dependencies and installs them using pip

**Challenge:** Maintaining face database across sessions  
**Solution:** Used pickle serialization to save face encodings to disk, allowing the program to remember enrolled users

**Challenge:** Robust camera initialization  
**Solution:** Added multi-step verification (camera open check, frame read test) with clear error messages

## Results

Successfully created a functional face recognition system that:
- Automatically handles dependency installation
- Persistently stores and loads face encodings
- Reliably initializes camera with error handling
- Can enroll and recognize multiple individuals
- Works across program restarts

## Skills Demonstrated

* Python file I/O and serialization
* Computer vision with OpenCV
* Face recognition algorithms
* Error handling and user experience design
* Package management and dependencies
* GUI development with Tkinter

## Future Improvements

* Add confidence scores for recognition matches
* Implement real-time video display with name labels
* Add ability to delete enrolled faces
* Create a full GUI for enrollment and management
* Add support for multiple camera sources
* Implement face anti-spoofing features
