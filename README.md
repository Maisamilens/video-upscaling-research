# Enhancing Video Resolution and Quality Using Video Up-scaling Techniques with MoviePy and OpenCV: A Case Study

## Overview

This repository contains code and documentation for the research study focused on enhancing video resolution and quality through advanced video up-scaling techniques. The methods employed utilize Python libraries such as **MoviePy** and **OpenCV** to transform low-resolution (480p) video content into high-definition (1080p) format. The research encompasses various video categories, including endoscopic videos, entertainment clips, and surveillance footage, demonstrating the effectiveness of these techniques in preserving visual quality.

## Research Objectives

1. To enhance the visual quality of low-resolution videos by up-scaling them to high-definition resolutions.
2. To evaluate the effectiveness of different interpolation techniques for video up-scaling.
3. To assess the computational performance and quality metrics (PSNR and SSIM) of the enhanced videos.

## Methodology

### Dataset Selection

The study involves the up-scaling of videos from various categories:
- **Endoscopic Videos**: Used in medical diagnostics.
- **Entertainment Clips**: Short films and movie scenes.
- **Surveillance Footage**: CCTV recordings.

### Pre-Processing Steps

1. **Video Selection and Resizing**: The original videos are resized to 480p for standardization.
2. **Frame Extraction**: Each video frame is extracted for individual processing.
3. **Quality Parameter Setting**: Video parameters such as frame rate and resolution are established.

### Video Up-scaling Techniques

The study employs three interpolation methods for up-scaling:
- **Bi-linear Interpolation**: A basic method that averages nearby pixels.
- **Bi-Cubic Interpolation**: A more advanced method that considers 4x4 pixel neighborhoods.
- **Lanczos Resampling**: A high-quality method that uses sinc functions for better clarity.

### Codec Optimization

The H.264 codec is used to optimize the video compression while preserving quality.

### Evaluation Metrics

The quality of the up-scaled videos is evaluated using:
- **Peak Signal-to-Noise Ratio (PSNR)**: Measures the quality of the reconstructed video.
- **Structural Similarity Index (SSIM)**: Assesses the structural similarity between the original and up-scaled videos.

## Installation and Requirements

To run the code, you need to install the following packages:

```bash
!pip install pydub moviepy yt-dlp opencv-python scikit-image
!apt-get install -y ffmpeg

Code Overview
Audio Enhancement: The improve_audio_quality function normalizes audio and applies filters.
Video Enhancement: The improve_video_quality function resizes videos to 1080p.
Metric Calculation: Functions to calculate PSNR and SSIM for quality assessment.

Example Usage
Here's an example of how to use the code:
# Improve audio quality
improved_audio_path = improve_audio_quality("/content/entertainment.mp4")

# Improve video quality
improve_video_quality("/content/entertainment.mp4", "/content/entertainment_improved.mp4")

# Compute metrics
avg_psnr, avg_ssim = compute_metrics("/content/original_video.mp4", "/content/improved_video.mp4")



