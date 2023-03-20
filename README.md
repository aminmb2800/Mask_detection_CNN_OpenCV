# Mask_detection_CNN_OpenCV

This project is a mask detection convolutional neural network (CNN) implemented with OpenCV, a popular computer vision library. The CNN is trained to detect whether a person is wearing a mask or not in real-time using a camera feed.

## Getting Started

To get started with this project, you will need to clone the repository and install the necessary libraries.

### Prerequisites

* Python 3
* OpenCV 4.0 or higher
* TensorFlow 2.0 or higher
* Keras 2.3 or higher
* NumPy 1.18 or higher

### Installing

1. Clone the repository to your local machine:

```
git clone https://github.com/aminmb2800/Mask_detection_CNN_OpenCV.git
```
2. Install the required libraries using pip:

```
pip install opencv-python tensorflow keras numpy
```
## Dataset 

The model is trained on the [Mask Detection Dataset](https://drive.google.com/drive/folders/1Eru9OyBdY5FDRegYcuZoEgR5pKCLPYfa?usp=sharing), which contains over 1376 images of people wearing masks and not wearing masks. The dataset is split into training and testing sets, with 80% of the images used for training and 20% for testing.

### Usage

To use the mask detection CNN, run the Face_mask_detection_CNN_OpenCV.ipynb script:

1. In the current of directory file, just need to run in terminal 'jupyter notebook Face_mask_detection_CNN_OpenCV.ipynb'  

### Model Architecture

The CNN model is built using TensorFlow's Keras API. It has the following architecture:


________________________________________________________________


| Layer (type)         | Output Shape               | Param                                |
| -------------------- | ---------------------------|------------------------------------- |
| conv2d (Conv2D)      |        (None, 62, 62, 32)  |      896                             |
| max_pooling2d (MaxPooling2D)| (None, 31, 31, 32)  |       0                              |
|conv2d_1 (Conv2D)     |       (None, 29, 29, 64)   |     18496                            |
|max_pooling2d_1 (MaxPooling2 |(None, 14, 14, 64)   |       0                              |
|conv2d_2 (Conv2D)     |        (None, 12, 12, 128) |     73856                            |
|max_pooling2d_2 (MaxPooling2 |(None, 6, 6, 128)    |       0                              |
|flatten (Flatten)     |       (None, 4608)         |       0                              |
|dense (Dense)         |       (None, 128)          |     589952                           |
|dropout (Dropout)     |       (None, 128)          |       0                              |
|dense_1 (Dense)       |       (None, 2)            |      258                             |

**Total params: 684,458**

**Trainable params: 684,458**

**Non-trainable params: 0**
