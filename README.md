# Text-Driven Image Synthesis: Generating Bird and Flower Images Using GAN

## Overview

We focused on creating realistic images of birds and flowers from text descriptions. To achieve this, we utilized advanced techniques known as text-to-image synthesis, where we trained a special kind of neural network called a conditional generative adversarial network (cGAN). This network learns to generate images based on the provided text captions. 
The network architecture we employed is based on [DCGAN](https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html#:~:text=What%20is%20a%20DCGAN%3F,al.), a proven framework for generating high-quality images. This architecture, shown below, forms the backbone of our text-to-image synthesis system, enabling us to produce resultant images.
<figure><img src='https://github.com/pthengane/Text2Image-GAN-PyTorch/blob/master/Results/DCGAN.jpg'></figure>
Credits: [1]

## Dataset Used

In this project, we utilized two main datasets: Caltech-UCSD Birds 200 and Oxford Flowers. These datasets are widely recognized in the computer vision community and provide rich collections of images for birds and flowers, respectively.

### 1. Caltech-UCSD Birds 200

The Caltech-UCSD Birds 200 dataset consists of images of birds belonging to 200 different species. It contains a diverse range of bird species captured in various poses and environments, making it a valuable resource for training models in bird recognition and synthesis.

### 2. Oxford Flowers

The Oxford Flowers dataset comprises images of flowers from 102 different categories. Each category represents a distinct type of flower, and the dataset contains multiple images per category captured under different conditions. This dataset is commonly used in research for tasks related to flower classification and image synthesis.

## Requirements

To run this project, ensure you have the following dependencies installed:

- torch==0.3.1.post3
- h5py==2.7.1
- easydict==1.9
- numpy==1.14.2
- Pillow==5.3.0
- PyYAML==3.13

You can install these dependencies using pip:

```bash
pip install torch==0.3.1.post3 h5py==2.7.1 easydict==1.9 numpy==1.14.2 Pillow==5.3.0 PyYAML==3.13
```

## Training

### Inputs for Training/Prediction:

- `dataset`: Choose the dataset to use (`birds` or `flowers`).
- `split`: An integer indicating which split to use (`0: train | 1: valid | 2: test`).
- `save_path`: Path for saving the trained models and results.
- `pre_trained_disc`: Path to the pre-trained discriminator model for initializing training or continuing from a checkpoint.
- `pre_trained_gen`: Path to the pre-trained generator model for initializing training or continuing from a checkpoint.
- `cls`: Boolean flag to indicate whether to train with classification algorithms or not.

Adjust these parameters according to your requirements and dataset setup. Happy training!

## Result 

These are some of the results generated by our model : 

![Output avi gif](https://github.com/pthengane/Text2Image-GAN-PyTorch/blob/master/Results/GAN_Results.gif)

## Acknowledgement

This project builds upon existing research in the field of text-to-image synthesis. We would like to express our sincere appreciation to the developers of the datasets used in this project, including the creators of the Caltech-UCSD Birds 200 and Oxford Flowers datasets. Their contributions have been invaluable in the development of this system.

We also extend our gratitude to the authors of the [Generative Adversarial Text-to-Image Synthesis paper](https://arxiv.org/abs/1605.05396) [1], which served as a guiding light and inspiration for our work. Additionally, we thank the creators of the [text embeddings](https://github.com/reedscot/icml2016) provided in the paper [1], which enhanced the capabilities of our model.

Feel free to explore, contribute, and adapt the project for specific use cases. Your support and contributions are highly appreciated.
