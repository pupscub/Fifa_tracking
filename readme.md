# FIFA Player Tracking with YOLOv5 and ByteTrack

A computer vision system that tracks football players, referees, goalkeepers and the ball in broadcast football matches using YOLOv5 object detection enhanced with ByteTrack multi-object tracking.

## Overview

This project combines:
- YOLOv5 with CSP (Cross Stage Partial Networks) backbone for robust object detection
- ByteTrack algorithm for accurate multi-object tracking
- Custom annotations for different football entities (players, ball, referees, etc.)

## Features

- Real-time tracking of multiple football entities
- Unique ID assignment to each tracked object
- Consistent tracking through occlusions and rapid movements
- Support for broadcast camera angles
- Ball possession detection

## Architecture

**Object Detection**: 
- YOLOv5 with CSP backbone[4]
  - Reduces duplicate gradients
  - Improves feature propagation
  - Optimizes parameter efficiency

**Object Tracking**:
- ByteTrack algorithm[1]
  - Two-stage tracking approach
  - Handles both high and low confidence detections
  - Maintains object identity through occlusions

## Installation

```bash
# Clone repository
git clone https://github.com/username/fifa-tracking
cd fifa-tracking

# Install dependencies
pip install -r requirements.txt

# Install YOLOv5
pip install yolov5

# Install ByteTrack
pip install bytetrack
