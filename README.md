# AI Gesture Mouse Control 🖱️👆

A sophisticated computer vision application that allows you to control your mouse cursor using hand gestures captured through your webcam. Built with Python, OpenCV, and MediaPipe, this project enables natural and intuitive interaction with your computer.

## ✨ Features

- **Hand Tracking**: Real-time detection and tracking of hand landmarks
- **Gesture-based Control**: Control mouse movement and clicks using natural hand gestures
- **Smooth Movement**: Implemented smoothening algorithm for precise cursor control
- **Performance Optimization**: Real-time FPS counter to monitor performance
- **Customizable Settings**: Adjustable parameters for sensitivity and control area

## 🚀 Getting Started

### Prerequisites

```bash
pip install opencv-python
pip install mediapipe
pip install numpy
pip install autopy
```

### Running the Application

1. Clone this repository
2. Navigate to the project directory
3. Run the main script:
```bash
python main.py
```

## 🎮 How to Use

1. **Moving the Cursor**:
   - Raise your index finger
   - Move your hand within the frame to control the cursor
   - The cursor position is smoothed for better precision

2. **Clicking**:
   - Raise both index and middle fingers
   - Bring them close together to perform a click
   - A green circle will appear when click is registered

## 🛠️ Technical Details

### Configuration Parameters

```python
wCam, hCam = 640, 480     # Camera resolution
frameR = 100              # Frame reduction for movement area
smoothening = 7           # Mouse movement smoothening factor
```

### Key Components

1. **HandTrackingModule.py**:
   - Custom module for hand detection and tracking
   - Implements MediaPipe solutions for hand landmark detection
   - Provides utilities for gesture recognition

2. **main.py**:
   - Main application logic
   - Implements mouse control functionality
   - Handles gesture interpretation and cursor movement

## 📝 Features Breakdown

### Hand Detection
- Uses MediaPipe's hand tracking solution
- Detects up to 21 hand landmarks
- Supports multiple hand tracking (configured for single hand in this application)

### Gesture Recognition
- Identifies finger positions and states (up/down)
- Calculates distances between landmarks
- Implements custom gesture patterns for mouse control

### Mouse Control
- Maps hand coordinates to screen coordinates
- Implements smoothening for precise movement
- Supports left-click functionality

## ⚙️ Customization

You can modify the following parameters in `main.py` to adjust the application behavior:

- `wCam, hCam`: Camera resolution
- `frameR`: Movement area boundary
- `smoothening`: Cursor movement smoothness

## 🔍 Troubleshooting

1. **Camera not working**:
   - Check if camera index is correct in `cv2.VideoCapture(0)`
   - Ensure camera permissions are granted

2. **Jerky cursor movement**:
   - Increase the `smoothening` value
   - Ensure adequate lighting conditions

3. **Performance issues**:
   - Check the FPS counter in the top-left corner
   - Reduce camera resolution if needed
   - Ensure no resource-heavy applications are running

## 📄 License

This project is open-source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 🙏 Acknowledgments

- MediaPipe team for their excellent hand tracking solution
- OpenCV community for computer vision tools
- Autopy developers for mouse control functionality
