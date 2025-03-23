# Road Lane Lines Detection using OpenCV

This project uses Python and OpenCV to detect lane lines on the road. It develops a processing pipeline that works on a series of individual images and applies the result to a video stream.

## Pipeline Architecture

The pipeline consists of the following steps:

1. **Load test images:** Loads a set of test images for processing.
2. **Apply Color Selection:** Isolates white and yellow lane lines using color thresholds in the HSL color space.
3. **Apply Canny edge detection:**
    - Converts images to grayscale.
    - Applies Gaussian smoothing to reduce noise.
    - Performs Canny edge detection to identify edges.
4. **Determine the region of interest:** Focuses on the area of the image containing the lane lines using a polygon mask.
5. **Apply Hough transform:** Detects line segments within the region of interest using the Hough transform.
6. **Average and extrapolate the lane lines:** Averages multiple detected lines for each lane and extrapolates them to cover the full lane length.
7. **Apply on video streams:** Processes video frames using the developed pipeline to detect lane lines in real-time.

## Getting Started

1. **Prerequisites:** Make sure you have Python 3 installed along with the following libraries:
    - OpenCV (`cv2`)
    - NumPy (`numpy`)
    - Matplotlib (`matplotlib`)
    - MoviePy (`moviepy`)
2. **Installation:** Install the required libraries using pip:
3.  **Running the code:** Execute the provided Python script in a Google Colab environment or Jupyter Notebook.
4. **Input:** Place your test images in the `test_images` folder and your test videos in the `test_videos` folder.
5. **Output:** The processed images and videos will be saved in the `output_images` and `output_videos` folders, respectively.

## Usage

The main functions for processing images and videos are:

- `frame_processor(image)`: Processes a single image frame to detect lane lines.
- `process_video(test_video, output_video)`: Processes an input video and saves the output video with detected lane lines.


# Acknowledgments

This project was inspired by the Udacity Self-Driving Car Engineer Nanodegree program.

I hope this README file provides a comprehensive overview of the project. Let me know if you need further assistance!
