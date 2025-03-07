# OpenCV Image Processing in Jupyter Lab

This repository contains Jupyter Notebook files and Python scripts demonstrating image processing techniques using OpenCV. The primary focus is on various image processing functions, including splitting and merging color channels, filtering, transformations, and more.

## Features

- Read images using OpenCV (`cv2.imread`)
- Split an image into its Blue, Green, and Red channels (`cv2.split`)
- Visualize the individual color channels using Matplotlib
- Merge color channels back into a complete image (`cv2.merge`)
- Display the merged image with the correct color format (`cv2.cvtColor`)
- Apply various image processing techniques such as:
  - Edge detection (Canny, Sobel, Laplacian)
  - Image filtering (GaussianBlur, MedianBlur, BilateralFilter)
  - Morphological operations (Erosion, Dilation, Opening, Closing)
  - Image transformations (Resizing, Rotating, Affine Transformations)
  - Object detection and contour analysis
  - Face and feature detection using OpenCV’s pre-trained models

## Requirements

To run the scripts, ensure you have the following dependencies installed:

```bash
pip install opencv-python matplotlib jupyterlab
```

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/opencv-jupyterlab.git
   cd opencv-jupyterlab
   ```
2. Launch Jupyter Lab:
   ```bash
   jupyter lab
   ```
3. Open the provided `.ipynb` file and execute the cells to see the output.

## Example Code

Here is a brief snippet from the project:

```python
import cv2
import matplotlib.pyplot as plt

# Read the image
img = cv2.imread("./image/test_2.png", cv2.IMREAD_COLOR)
b, g, r = cv2.split(img)

# Plot the individual color channels
plt.figure(figsize=[20, 5])
plt.subplot(1, 4, 1); plt.imshow(b, cmap='gray'); plt.title("Blue Channel"); plt.axis("off")
plt.subplot(1, 4, 2); plt.imshow(g, cmap='gray'); plt.title("Green Channel"); plt.axis("off")
plt.subplot(1, 4, 3); plt.imshow(r, cmap='gray'); plt.title("Red Channel"); plt.axis("off")

# Merge and show the image
merged_img = cv2.merge((b, g, r))
plt.subplot(1, 4, 4); plt.imshow(cv2.cvtColor(merged_img, cv2.COLOR_BGR2RGB)); plt.title("Merged Image"); plt.axis("off")
plt.show()
```

## Folder Structure

```
/opencv-jupyterlab
│── image/              # Folder containing test images
│── notebooks/          # Jupyter notebooks with OpenCV examples
│── scripts/            # Python scripts for OpenCV processing
│── README.md           # Project documentation
```

## License

This project is open-source and available under the [MIT License](LICENSE).

## Contributing

Feel free to open issues or submit pull requests to improve the project!

## Author

[VOYAGER aka Mainak ](https://github.com/VOYAGER441)

