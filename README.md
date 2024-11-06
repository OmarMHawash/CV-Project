# CV Project

This project performs a complete pipeline for image stitching, edge detection, and human detection. It begins by stitching three ordered images (left, center, right) from the specified folder into a single panorama. This stitched image then undergoes edge detection using the Difference of Gaussians (DoG) method, with customizable sigma values to control edge detail. Finally, the processed image is passed through a YOLO-based model for human detection

### Prerequisites:

- recommended Python v`3.11.8` or newer.

### Local Installation Steps:

1. Clone the project: `git clone <repo_url>`
2. Setup python app:

```
python -m venv venv # MacOS: python3 -m venv venv
.\venv\Scripts\activate # MacOS: source venv/bin/activate
pip install -r .\requirements.txt
```

## Test preview:

### 1. Input images:
<img src='https://github.com/OmarMHawash/CV-Project/blob/main/test/1.png' height='150px' /> --- <img src='https://github.com/OmarMHawash/CV-Project/blob/main/test/2.png' height='150px' /> --- <img src='https://github.com/OmarMHawash/CV-Project/blob/main/test/3.png' height='150px' />

### 2. Images Stitcing:
image stitching to create **panoramas** by aligning and merging multiple images. It supports sequential stitching of two or three images, with **configurable confidence thresholds** and detailed debugging output to monitor each stitching step.

Output result:

<img src='https://github.com/OmarMHawash/CV-Project/blob/main/results/stitched.jpg?raw=true' height='200px' />

### 3. Edge Detection:
edge detection pipeline using the **Difference of Gaussians (DoG)** method. The pipeline applies Gaussian blurring with **two sigma values**, calculates their difference to highlight edges, and cleans up the result with **morphological operations**.

Output result:

<img src='https://github.com/OmarMHawash/CV-Project/blob/main/results/edge_result.jpg' height='200px' />

### 4. human Detection:
human detection on an input image using a YOLO model `yolov8x`, with bounding boxes drawn around detected people. The model, **confidence threshold** is configurable

Output result:

<img src='https://github.com/OmarMHawash/CV-Project/blob/main/results/detect_result.jpg' height='200px' />
