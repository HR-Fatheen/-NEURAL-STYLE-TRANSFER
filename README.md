# Neural Style Transfer 

## Internship Credentials

- **Intern Name**: Mohamed Fatheen H.R  
- **Intern ID**: CT06DG2241  
- **Domain**: AI Developer Intern  
- **Company**: CodTech IT Solutions  
- **Internship Duration**: 4 Weeks  
- **Mentor**: Neela Santosh Kumar 


## Description

**Neural Style Transfer (NST)** is a fun technique built with PyTorch that lets you take the artistic style from one image—like a famous painting—and blend it with another image, such as a photo of the city skyline. This process combines the power of deep learning with creativity by using a pre-trained neural network, specifically VGG-19, to analyze and extract features from both images.

The core idea behind Neural Style Transfer is to separate and then merge the content of one image with the style of another. To do this, I wrote a Python script that does a few key things:

  - Loads and prepares the images for processing. - Uses a pre-trained model to extract important features.
  - Calculates how similar the style and content are using specific loss functions.
  - Iteratively tweaks a new image to minimize these losses, gradually blending style into content.

For this project, I used Vincent van Gogh's famous painting "The Starry Night" as the style image, and a photograph of the New York skyline as the content image. During 300 to 750 training steps with the Adam optimizer, the script gradually developed an output image that captured the swirling brushstrokes and color palette of Van Gogh’s work, all while keeping the main structure of the cityscape intact. The process includes these steps :

  - **Image Preprocessing**: Used `PIL` and `torchvision.transforms` to resize and convert images into tensors.
  - **Feature Extraction**: VGG-19 model layers were used to extract activations relevant to both style and content.
  - **Loss Functions**:  
    - Content Loss: Mean Squared Error between features from `conv4_2`.
    - Style Loss: Gram Matrix differences across `conv1_1`, `conv2_1`, `conv3_1`, `conv4_1`, and `conv5_1`.
  - **Optimization**: The output image was optimized directly as a trainable tensor over multiple iterations.

The result successfully reflected **artistic texture and color from the style image** while **preserving the shapes and layout from the content image**. Adjustments to `style_weight`, `content_weight`, and `steps` were made to amplify the artistic effect.


### Coded Platform Details

- **Programming Language**   : Python 3.12  
- **Libraries Used**         : `torch`, `torchvision`, `matplotlib`, `PIL`  
- **Model Used**             : Pre-trained **VGG-19** from `torchvision.models`  
- **Deep Learning Framework**: **PyTorch**  
- **IDE/Editor**             : Jupyter Notebook (Anaconda distribution)  
- **Execution Platform**     : Windows 11 (Local Machine)  
- **Style Image Used**       : *The Starry Night* by Vincent van Gogh  
- **Content Images**         : Custom images (.jpg format)  
- **Epochs/Steps**           : 750 (for best pattern visibility)


## Files Structure

* Task 3               
 ─ README.md                
 ─ coding.ipynb             
 ─ Installation & Setup
 ─ Sample Inputs & Output

## How It Works

1. **Load content and style images** using `load_image()` with resizing and tensor conversion.
2. **Extract VGG features** via a customized `VGGFeatures` class.
3. **Compute content and style loss** using selected layers.
4. **Generate an image** by cloning the content image and training it to minimize total loss.
5. **Visualize output** with `matplotlib`.


## 📌 Parameters Used

| Parameter         | Value     |
|------------------|-----------|
| content_weight    | 1e4       |
| style_weight      | 1e2       |
| optimizer         | Adam      |
| learning_rate     | 0.01      |
| steps             | 300–750   |


##  Output Result
![Image](https://github.com/user-attachments/assets/abcc9fd6-88f3-4ff4-b975-0de8fddcce94)

## Notes

- For stronger style patterns, increase `style_weight` or `steps`.
- For faster rendering, reduce image size, but it may lower quality.
- You must use RGB `.jpg` or `.png` images to avoid loading errors.

## Developed By

**Mohamed Fatheen H.R**  
AI Developer Intern @ CodTech IT Solutions  
2025
