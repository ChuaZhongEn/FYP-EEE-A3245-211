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
This notebook must be run in a separate IDE (e.g. Visual Studio Code).

![Screenshot (138)](https://user-images.githubusercontent.com/67497833/161477373-9a54c27a-ff19-4c82-a6a7-b662d12a4a5c.png)

The pretrained network can be downloaded [here](https://drive.google.com/file/d/1igxv6ZP4TFGe_392B-qnSqXnglTKH5yo/view?usp=sharing) and must be placed in the GUI Resources folder. 
