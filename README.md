# CodeAlpha_HandwrittenCharacter_Detection

This repository contains code for handwritten character detection using Python, particularly focusing on shuffling and visualizing a subset of images from a dataset. The project utilizes popular libraries such as NumPy, OpenCV, and Matplotlib.
#Code Overview:
Shuffling the Dataset:
The code uses the shuffle function to randomly reorder the first 100 elements of the training data (train_x).
 ```python
   shuff = shuffle(train_x[:100])
```
Visualizing Shuffled Images:
The script then creates a 3x3 grid of subplots using Matplotlib to visualize a subset of the shuffled images.
```python 
fig, ax = plt.subplots(3, 3, figsize=(10, 10))
axes = ax.flatten()
```

Thresholding Operation:
A loop iterates over the first 9 shuffled images, applies a binary thresholding operation using OpenCV, and displays the reshaped images in the corresponding subplots.
```python
for i in range(9):
    _, shu = cv2.threshold(shuff[i], 30, 200, cv2.THRESH_BINARY)
    axes[i].imshow(np.reshape(shuff[i], (28, 28)), cmap="Greys")
```

How to Use:
Clone the repository to your local machine:
```
git clone https://github.com/Praneetha1844/CodeAlpha_HandwrittenCharacter_Detection.git
```
Ensure you have the required dependencies installed:
```
pip install numpy opencv-python matplotlib
```
## Dataset

Due to the size of the dataset, it is not included directly in this repository. You can download the dataset from the following link:

[Download Dataset](https://www.kaggle.com/sachinpatel21/az-handwritten-alphabets-in-csv-format)

Please follow the instructions in the documentation to properly integrate the dataset with the code.
