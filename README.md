# FYP-EEE-A3245-211 <br> Face Transformation using StyleGAN

## Nanyang Technological University

This repository contains the scripts used in Final Year Project - Face Transformation using StyleGAN.

![Picture1](https://user-images.githubusercontent.com/67497833/161471635-5c19489d-884f-4ee1-8b44-da977afb83ab.png)

## Data Repository
| Path | Description
| :--- | :----------
| GUI Resources | Resources used in the GUI application
| &ensp;&ensp;&boxvr;&nbsp; default_settings.npy | File used to hold previous settings
| &ensp;&ensp;&boxvr;&nbsp; stylesheet.css | Stylesheet for the GUI application
| Learned Coefficients | Learned SVC/SVR coefficients for face transformation
| &ensp;&ensp;&boxvr;&nbsp; SVC | Folder containing all learned SVC coefficients
| &ensp;&ensp;&boxvr;&nbsp; SVR | Folder containing all learned SVR coefficients
| [stylegan2-ada-pytorch](https://nvlabs-fi-cdn.nvidia.com/stylegan2-ada-pytorch/) | Cloned stylegan2-ada-torch repo
| 0_Image_Generator.ipynb | Google Colab notebook for generating StyleGAN2 images
| 1_Learnging_StyleGAN_Image_Synthesis_Controls.ipynb | Google Colab notebook for learning controls for face transformation using StyleGAN2
| 2_StyleGAN_Image_Projection.ipynb | Google Colab notebook for StyleGAN2 Projection method
| 3_Face_Transformation_GUI.ipynb | Notebook for Face Transformation GUI application

## Requirements
Libraries version used:

1. PyTorch 1.10.0
2. Numpy 1.21.4
3. Pathlib
4. PIL 8.0.0
5. Matplotlib 3.5.0
6. PyQt5

## How to use
The following notebooks are designed to be run in a Google Colab notebook without any modifications required. <br>
1. 0_Image_Generator.ipynb
   - Optional: Use this notebook to generate and save StyleGAN2 images.
3. 1_Learnging_StyleGAN_Image_Synthesis_Controls.ipynb
   - This notebook contain the steps involved in learning control for StyleGAN2 image synthesis using Support Vector Regression (SVR) and Support Vector Classifier (SVC).
5. 2_StyleGAN_Image_Projection.ipynb
   - This notebook contain the steps involved in projecting a real photograph into the StyleGAN2 latent space.

## Face Transformation GUI
Note: This GUI is built using PyQt which is not supported in Google Colab. <br>
This notebook must be run in a separate IDE (e.g. Visual Studio Code). <br>

This GUI serves as a tool to visualize the Face Transformation using the learned coefficients. <br>
Loading of a transformed seed or projected face is not supported. <br>

The pretrained network can be downloaded [here](https://drive.google.com/file/d/1igxv6ZP4TFGe_392B-qnSqXnglTKH5yo/view?usp=sharing).

![Picture2](https://user-images.githubusercontent.com/67497833/161480413-8410f33f-7b17-4793-8473-7801bb896e40.png)

How to use the GUI
1. Select the downloaded pretrained network 
   - Upon select, the network will be initialised automatically. 
   - NOTE: The GUI may freeze temporarily as the network is being initialized.
2. Select the coefficient foldder
   - Select either the SVC or SVR folder
   - The files within the selected folder will be loaded and the GUI will be updated automatically.
3. Generate an image OR Load a projected image
   - 3.1. To generate an image
      - Select the Generate Seed Tab, choose the desired seed using the spinbox and click on 'Generate' button
   - 3.2. To load an projected image
      - Select the Load Projected Face Tab, select the projected .npz file and click on 'Load' button
4. Adjust the sliders/spinbox on the left to transform the generated/loaded face.
   - The transformed face will be updated automatically.
5. Save the transformation data .
   - The save directory must be selected.
   - Go to the desired row and click 'Save'.

Extra:
1. (E1) To transform multiple faces, click on the 'Add New Seed' button.
   - Only works when the latest added seed is generated/loaded.
2. (E2) To reset the GUI, click on the 'Reset' button.
   - NOTE: All unsaved data will be lost.
3. The following transformation data is saved:
   - Coefficients data (Coefficient, Intensity, Scale)
   - Image data (Seed, Original Latent Vector, Transformed Latent Vector)
   - A PNG image of the original and transformed face.
