# Video-Audio Matching Dataset

## Overview
This dataset contains video and audio files that were originally jumbled. The goal was to correctly match each audio file to its corresponding video file by analyzing the timing of ball bounces in both modalities.

## Dataset Structure
The dataset consists of the following components:

1. **Cropped Videos (`cropped_videos/`)**: 
   - The videos contain a ball bouncing off the edges of a box.
   - Each video has been cropped to focus only on the box.

2. **Video Analysis**:
   - When the ball bounces, it disappears for one frame.
   - **Binary Video Plots (`vid_binary_plots/`)**:
     - A plot showing the average pixel intensity per frame.
     - Frames where the ball disappears have the highest intensity.
   - **Binary Video Data (`vid_txt/`)**:
     - A text file containing binary values (0 or 1) based on pixel intensity thresholding.
     - 2400 frames over 20 seconds.

3. **Audio Analysis**:
   - The audio files contain sound events that correspond to ball bounces.
   - **Binary Audio Plots (`binary_audio_plots/`)**:
     - A plot of the audio amplitude after noise removal.
     - Binary representation of the detected bounce sounds.
   - **Binary Audio Data (`aud_txt/`)**:
     - A text file containing binary values from thresholding the audio signal.
     - 320,000 rows representing the time sequence of detected bounce sounds.

4. **Matching Algorithm**:
   - A cross-correlation algorithm was applied to align the video and audio events.
   - The results are stored in `matching_results.csv`, mapping video files to their correct audio counterparts.

## Usage
To use this dataset:
1. Use `vid_txt/` and `aud_txt/` to analyze bounce timing.
2. Refer to `matching_results.csv` for correctly paired video-audio files.
3. Visualize bounce events using `vid_binary_plots/` and `binary_audio_plots/`.

## Files and Directories
```
📂 Dataset Root
 ├── 📂 cropped_videos/         # Cropped video files
 ├── 📂 vid_binary_plots/       # Plots of video frame intensities
 ├── 📂 vid_txt/                # Binary text files for video analysis
 ├── 📂 binary_audio_plots/     # Plots of audio bounce events
 ├── 📂 aud_txt/                # Binary text files for audio analysis
 ├── 📄 matching_results.csv    # Mapped video-audio pairs
```


