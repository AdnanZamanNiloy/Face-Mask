
# Face Mesh Detection using OpenCV & MediaPipe

This project implements real-time face mesh detection using OpenCV and MediaPipe. It captures input from the webcam (or a video file) and detects 468 facial landmarks on each face.

## Key Features

- Supports multiple faces (default: 2)
- Prints facial landmark coordinates
- Displays FPS counter
- Easy to extend for face recognition or emotion detection


## Installation

Install the required Python packages using pip:

```bash
pip install opencv-python mediapipe
```

## Usage

To run face mesh detection using your webcam:

```bash
python Facemesh.py
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
| `demo_image.png`       | Sample video demonstrating the output     |


## Sample Output
![image](https://github.com/user-attachments/assets/0f65b93a-c61a-47bc-9e07-0d7f3ce5b90d)

## Future Enhancements

- Integrate with attendance system
- Save detected faces with timestamps
- Improve live-ness detection with more eye and head movement checks

## License

This project is released for educational and academic purposes.
