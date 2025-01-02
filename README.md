# Hand-Gesture-Volume-Control

# Hand Gesture Volume Control

A Python application that allows users to control their system's volume through hand gestures captured via webcam. This project utilizes computer vision and hand tracking to create an interactive way to adjust audio volume.

## Description

The Hand Gesture Volume Control project uses a webcam to detect hand movements and converts the distance between specific fingers into volume adjustments. It employs MediaPipe for hand landmark detection and OpenCV for image processing, creating an intuitive interface for volume control through natural hand movements.

### Key Features

- Real-time hand tracking and gesture recognition
- Volume control through finger distance measurement
- Visual feedback with on-screen display
- FPS counter for performance monitoring
- Volume level visualization

## Prerequisites

Before running this project, ensure you have the following dependencies installed:

```bash
pip install opencv-python
pip install mediapipe
pip install numpy
pip install pycaw
pip install comtypes
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/hand-gesture-volume-control.git
cd hand-gesture-volume-control
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

## Usage

1. Run the volume control application:
```bash
python volumeControl.py
```

2. Hold your hand up to the webcam
3. Use your thumb and index finger to control the volume:
   - Increase the distance between fingers to increase volume
   - Decrease the distance between fingers to decrease volume
   - The minimum distance threshold is 50 pixels
   - The maximum distance threshold is 300 pixels

## Project Structure

- `volumeControl.py` - Main application file for volume control
- `handtrackingmodule.py` - Module containing the hand tracking implementation
- `main.py` - Basic implementation of hand tracking
- `dummyCodeHandDetector.py` - Testing file for hand detection

## Technical Details

The project utilizes several key technologies:

- **OpenCV** - For webcam capture and image processing
- **MediaPipe** - For hand landmark detection
- **pycaw** - For Windows audio control
- **NumPy** - For mathematical operations and interpolation

The hand tracking system detects 21 different landmarks on each hand, with specific focus on landmarks 4 (thumb tip) and 8 (index finger tip) for volume control.

## Performance Notes

- Recommended webcam resolution: 648x488 pixels
- Target FPS: 30+
- Optimal lighting conditions recommended for better hand detection
- Minimum detection confidence: 0.7 (configurable)

## Limitations

- Currently supports Windows operating systems only due to pycaw dependency
- Requires good lighting conditions for optimal hand detection
- May experience slight latency depending on system specifications
- Single hand detection mode by default

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
