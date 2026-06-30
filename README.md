# Exercise Analysis System — YOLOv8 Pose Estimation

A computer vision project for analyzing squat and push-up exercises using YOLOv8 pose estimation.

## Project Overview

The system processes exercise videos to:

- Detect human body keypoints
- Calculate joint angles
- Count squat and push-up repetitions
- Evaluate exercise form
- Generate structured JSON results
- Produce an annotated output video

## Features

- YOLOv8s Pose Estimation
- 2D body keypoint detection
- Squat repetition counting
- Push-up repetition counting
- Exercise form assessment
- Exponential Moving Average smoothing
- Left/right body-side visibility selection
- Joint-angle calculation
- Annotated video output
- Structured JSON summary

## Exercise Analysis

### Squats

Squat repetitions are detected using knee-angle changes.

Form quality is evaluated using:

- Knee depth
- Back angle
- Exercise movement sequence

### Push-ups

Push-up repetitions are detected using elbow-angle changes.

Form quality is evaluated using:

- Elbow depth
- Shoulder–hip–ankle body alignment
- Exercise movement sequence

## Output

The system generates:

- Total squat repetitions
- Correct-form squat repetitions
- Total push-up repetitions
- Correct-form push-up repetitions
- Annotated exercise video
- JSON analysis file

Example:

```json
{
  "summary": {
    "squats": {
      "total_reps": 5,
      "good_form_reps": 4
    },
    "pushups": {
      "total_reps": 5,
      "good_form_reps": 4
    }
  }
}
