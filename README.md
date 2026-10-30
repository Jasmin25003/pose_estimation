# Human Pose Estimation with YOLO

This project uses Ultralytics YOLO pose estimation to detect human body
keypoints in a video and connect them into a skeleton. It generates two
processed videos: a skeleton on a black background and a skeleton overlaid on
the original video.

## Project files

| File | Description |
| --- | --- |
| `pose_estimation.ipynb` | Notebook with the pose-detection and video-processing code |
| `input.mp4` | Source video processed by the notebook |
| `pose_output.mp4` | White skeleton on a black background |
| `pose_overlay.mp4` | Source video with the white skeleton overlaid |

## Installation

Install Python and the required packages:

```bash
python -m pip install ultralytics opencv-python numpy
```

## How to run

1. Make sure `input.mp4` is in the same working directory as the notebook.
2. Make the `yolo26n-pose.pt` model weights available in that directory. The
   weights are used by the notebook but are not included in this repository.
3. Open `pose_estimation.ipynb` in Jupyter Notebook or JupyterLab and run its
   code cell.

The notebook processes the video and writes `pose_output.mp4` and
`pose_overlay.mp4` to the current working directory. It uses a confidence
threshold of `0.25` for keypoints.

## Videos

- [Original input video](input.mp4)
- [Pose overlay](pose_overlay.mp4)
- [Skeleton on black background](pose_output.mp4)

## Model and pose drawing

The notebook loads the pretrained `yolo26n-pose.pt` pose-estimation model. It
draws keypoints and the defined skeleton connections when the relevant
keypoint confidence scores are above `0.25`. No model training is performed
in this project.
