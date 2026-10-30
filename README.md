# Pose Estimation with YOLO

This project uses Ultralytics YOLO pose estimation to detect people and draw their
keypoints and skeleton on a video.

## Project files

- `pose_estimation.ipynb` — notebook containing the video-processing code.
- `input.mp4` — source video.
- `pose_output.mp4` — output showing the detected skeleton on a black background.
- `pose_overlay.mp4` — source video with the detected skeleton overlaid.

The `yolo26n-pose.pt` model weights are not included in this repository. Make
the weights available in the project directory before running the notebook.

## Requirements

Install the Python packages used by the notebook:

```bash
pip install ultralytics opencv-python numpy
```

## Run

1. Keep `input.mp4` and the `yolo26n-pose.pt` model weights in the same directory
   as the notebook.
2. Open `pose_estimation.ipynb` in Jupyter Notebook or JupyterLab.
3. Run the code cell. The notebook writes `pose_output.mp4` and
   `pose_overlay.mp4` to the current working directory.

The notebook uses a confidence threshold of `0.25` for pose keypoints.
