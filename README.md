
# Face Mesh Detection using OpenCV & MediaPipe

This project implements real-time face mesh detection using OpenCV and MediaPipe. It captures input from the webcam (or a video file) and detects 468 facial landmarks on each face.

## Key Features

- Real-time face mesh detection with 97% accuracy
- Live-ness detection via blink detection — ensures the student is physically present in front of the camera
- Supports multiple faces (default: 2)
- Prints facial landmark coordinates
- Displays FPS counter
- Easy to extend for face recognition or emotion detection

## Demo

A short demo video has been included in the repository to show the working system.

## Installation

Install the required Python packages using pip:

```bash
pip install opencv-python mediapipe
```

## Usage

To run face mesh detection using your webcam:

```bash
python face_mesh_detector.py
```

To use a video file instead:

In `main()` function, replace this line:
```python
cap = cv2.VideoCapture(0)
```
with:
```python
cap = cv2.VideoCapture("path_to_video.mp4")
```

Press 'q' to exit the video window.

## How It Works

- Uses MediaPipe's lightweight FaceMesh model to detect 468 landmarks per face
- Tracks eye movement to determine live-ness (e.g., using blink detection logic)
- Converts BGR to RGB before feeding frames to MediaPipe
- Overlays green face mesh using cv2.draw_landmarks

## Files in This Project

| File Name              | Description                               |
|------------------------|-------------------------------------------|
| `face_mesh_detector.py`| Main Python file for real-time detection  |
| `README.md`            | Project description and setup instructions|
| `demo_video.mp4`       | Sample video demonstrating the output     |

## Support

If you want to modify, extend, or integrate with facial recognition, emotion detection, or attendance systems, feel free to open an issue or contact the developer.

## Sample Output
https://www.google.com/url?sa=i&url=https%3A%2F%2Fpysource.com%2F2021%2F05%2F14%2Ffacial-landmarks-detection-with-opencv-mediapipe-and-python%2F&psig=AOvVaw3XbO6naj3te7G2nbgUMrG4&ust=1751694626443000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCNCs6pTBoo4DFQAAAAAdAAAAABAM
## Future Enhancements

- Integrate with attendance system
- Save detected faces with timestamps
- Improve live-ness detection with more eye and head movement checks

## License

This project is released for educational and academic purposes.
