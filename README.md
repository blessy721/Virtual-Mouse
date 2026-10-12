
# 🖱️ Virtual Mouse Using Hand Gesture Recognition

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/MediaPipe-0097A7?style=for-the-badge" alt="MediaPipe"/>
  <img src="https://img.shields.io/badge/PyAutoGUI-333333?style=for-the-badge" alt="PyAutoGUI"/>
</p>

<p align="center">
  <strong>Control your computer using hand gestures and a webcam — without a physical mouse.</strong>
</p>

---

## 📌 Project Overview

**Virtual Mouse** is a computer vision-based application that enables users to interact with a computer through hand gestures captured by a webcam or built-in camera.

The system detects hand landmarks, recognizes predefined gestures, and translates hand movements into mouse operations. It is designed to explore an alternative input method for human-computer interaction (HCI), combining computer vision, gesture recognition, and desktop automation.

Developed using Python, OpenCV, MediaPipe, and PyAutoGUI, the project demonstrates how visual hand tracking can be used to control cursor movement, perform mouse clicks, scroll content, and adjust selected system settings.

## 🎯 Problem Statement

Traditional computer interaction depends heavily on physical input devices such as a mouse. Alternative interaction methods can be useful in touch-free environments and in exploring more accessible human-computer interfaces.

This project addresses the problem by using a camera to detect hand movements and gestures, converting them into corresponding computer control actions without requiring a conventional mouse.

## 🎯 Objectives

- Develop a webcam-based virtual mouse using computer vision.
- Detect and track hand landmarks in real time.
- Recognize predefined hand gestures for mouse operations.
- Map hand movement to screen cursor movement.
- Support mouse clicking, dragging, and scrolling through gestures.
- Explore gesture-based control of system volume and screen brightness.
- Demonstrate an alternative approach to human-computer interaction.

## ✨ Key Features

| Feature | Description |
|---|---|
| 🖐️ Hand Tracking | Detects hand landmarks using MediaPipe |
| 🖱️ Cursor Movement | Maps hand movement to screen coordinates |
| 👆 Left Click | Performs a click using a recognized finger gesture |
| 🖱️ Right Click | Triggers the right mouse button through gesture recognition |
| 🖱️ Double Click | Recognizes a predefined two-finger gesture |
| ✋ Drag and Drop | Uses a fist gesture to hold and move the mouse |
| 📜 Scrolling | Supports vertical and horizontal scrolling through pinch movement |
| 🔊 Volume Control | Adjusts system volume through gesture-based movement |
| ☀️ Brightness Control | Adjusts screen brightness through gesture-based movement |
| 🎥 Live Camera Feed | Processes webcam frames and displays hand landmarks |

*The available controls depend on the implemented gesture mappings, system compatibility, and required permissions.*

## 🛠️ Technology Stack

### Programming Language

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
</p>

### Libraries and Tools

<p>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/MediaPipe-0097A7?style=for-the-badge" alt="MediaPipe"/>
  <img src="https://img.shields.io/badge/PyAutoGUI-333333?style=for-the-badge" alt="PyAutoGUI"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
</p>

| Technology | Purpose |
|---|---|
| Python | Core programming and application logic |
| OpenCV | Webcam input, image processing, and frame display |
| MediaPipe | Hand landmark detection and tracking |
| PyAutoGUI | Mouse movement, clicks, and scrolling |
| Math | Distance calculations and gesture recognition |
| PyCAW | Windows system audio volume control |
| Screen Brightness Control | System display brightness adjustment |
| Protocol Buffers | Processing MediaPipe hand classification results |
| Visual Studio Code | Development environment |

## ⚙️ System Workflow

```text
        ┌────────────────────────┐
        │      Webcam Input      │
        └───────────┬────────────┘
                    │
                    ▼
        ┌────────────────────────┐
        │  Capture Camera Frames │
        └───────────┬────────────┘
                    │
                    ▼
        ┌────────────────────────┐
        │   OpenCV Processing    │
        └───────────┬────────────┘
                    │
                    ▼
        ┌────────────────────────┐
        │ MediaPipe Hand Tracking│
        │  and Landmark Detection│
        └───────────┬────────────┘
                    │
                    ▼
        ┌────────────────────────┐
        │ Gesture Recognition    │
        │ Finger and Pinch State │
        └───────────┬────────────┘
                    │
                    ▼
        ┌────────────────────────┐
        │ Gesture-to-Action      │
        │ Mapping                │
        └───────────┬────────────┘
                    │
                    ▼
        ┌────────────────────────┐
        │ Cursor, Click, Scroll, │
        │ Volume and Brightness  │
        └────────────────────────┘
```

## 🔄 Methodology

The application follows these processing stages:

1. **Camera Initialization:** Open the webcam and capture video frames.
2. **Frame Preprocessing:** Flip frames horizontally and convert them into the format required for hand tracking.
3. **Hand Landmark Detection:** Use MediaPipe Hands to detect and track hand landmarks.
4. **Gesture Recognition:** Analyze finger positions, relative distances, and landmark coordinates to identify predefined gestures.
5. **Cursor Mapping:** Convert hand landmark coordinates into screen coordinates and apply movement smoothing.
6. **Action Execution:** Use PyAutoGUI to perform cursor movement, clicks, dragging, and scrolling.
7. **System Control:** Use the relevant system libraries to adjust volume or brightness when the corresponding gestures are recognized.
8. **Live Visualization:** Display the camera feed with detected hand landmarks and allow the application to exit using the Enter key.

## 🖐️ Gesture Controls

The following table summarizes the gesture mappings implemented in the current source code.

| Hand Gesture | Action |
|---|---|
| ✌️ V gesture | Move the cursor |
| ✊ Fist | Hold the left mouse button and drag |
| ☝️ Index finger | Right click |
| 🖕 Middle finger | Left click |
| 🤏 Closed two-finger gesture | Double click |
| 🤏 Pinch gesture — minor hand | Horizontal or vertical scrolling |
| 🤏 Pinch gesture — major hand | Adjust volume or screen brightness |

**Note:** Pinch direction and the selected hand determine the associated scrolling or system-control behavior. Actual behavior may vary with hand tracking and system configuration.

## 💻 Requirements

- Python installed on your system
- A webcam or built-in camera
- Visual Studio Code or another Python development environment
- A compatible desktop operating system
- Internet access to install the required packages

**Platform note:** The current implementation uses PyCAW and COM interfaces for audio control, which are Windows-specific. Brightness control also depends on hardware and operating-system support.

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/blessy721/virtual-mouse.git
cd virtual-mouse
```

If your repository has a different name, replace the URL and directory name with the actual values.

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Activate it on Linux or macOS:

```bash
source venv/bin/activate
```

### 3. Install the Required Libraries

The current Python implementation imports the following packages:

```bash
pip install opencv-python mediapipe pyautogui
pip install pycaw comtypes screen-brightness-control
pip install protobuf
```

The compatible versions of MediaPipe and its dependencies may vary by Python version. If installation fails, use a Python version supported by your chosen MediaPipe release.

### 4. Run the Application

If your main Python file is named `Virtual_Mouse.py`, execute:

```bash
python Virtual_Mouse.py
```

Allow camera access if prompted.

### 5. Exit the Application

Press the **Enter key** while the camera window is active to stop the program and close the webcam window.

## 📂 Project Structure

```text
Virtual-Mouse/
│
├── Virtual_Mouse.py
├── README.md
├── requirements.txt
├── .gitignore
└── assets/
    ├── virtual-mouse-demo.png
    └── gesture-controls.png
```

This is a suggested structure. Keep the filenames and folders consistent with the actual repository. Add screenshots to the `assets/` directory if you have them.

## 📸 Screenshots and Demonstration

Add screenshots or a short demonstration video to show the application working.

Recommended visuals:

- Webcam feed with detected hand landmarks
- Cursor movement controlled by hand gestures
- Demonstration of click and drag operations
- Volume or brightness control using pinch gestures

For example, if you upload a screenshot to `assets/virtual-mouse-demo.png`, display it using:

```markdown
![Virtual Mouse Demonstration](assets/virtual-mouse-demo.png)
```

## 📊 Results and Discussion

The project demonstrates the integration of computer vision and desktop automation to create a gesture-based input system.

The implementation includes:

- Live webcam capture and hand landmark tracking.
- Recognition of predefined hand gestures.
- Mapping of hand movement to mouse cursor movement.
- Mouse click, double-click, drag, and scrolling operations.
- Gesture-based system volume and brightness adjustment.

The system offers an alternative interaction method without requiring a physical mouse. Its performance depends on camera quality, lighting conditions, hand visibility, gesture recognition stability, and system compatibility.

Formal accuracy, latency, and performance improvements should be reported only after conducting and documenting appropriate tests.

## 🔮 Future Enhancements

- Improve gesture recognition stability and cursor precision.
- Add configurable gesture mappings.
- Introduce an on-screen interface for gesture status and settings.
- Add calibration for different screen sizes and camera positions.
- Improve error handling and compatibility checks.
- Add automated tests for gesture recognition and control logic.
- Evaluate response time and gesture recognition accuracy under different conditions.

## 🔒 Privacy and Safety

- Camera frames are processed by the local application; verify any additional components before making privacy claims.
- Use the system only on devices you are authorized to control.
- Keep a physical mouse or keyboard available as a fallback.
- Review automation behavior before using the application with important documents or system settings.

## 🎓 Learning Outcomes

This project provided an opportunity to explore:

- Computer vision and real-time video processing.
- Hand landmark detection and gesture recognition.
- Coordinate mapping and cursor movement.
- Python library integration.
- Human-computer interaction concepts.
- Desktop automation and operating-system controls.

## 👩‍💻 Author

**Blessy Jefrina H**
Bachelor of Engineering
Computer Science and Engineering

- GitHub: [@blessy721](https://github.com/blessy721)
- LinkedIn: [Blessy Jefrina](https://www.linkedin.com/in/blessyjefrina/)
- Email: [blessyjefrina0821@gmail.com](mailto:blessyjefrina0821@gmail.com)

---

<p align="center">
  <strong>Exploring Computer Vision • Building Intuitive Interfaces • Innovating Human-Computer Interaction</strong>
</p>
