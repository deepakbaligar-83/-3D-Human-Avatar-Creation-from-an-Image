# Human 3D Avatar Generation from an Image

This project implements a robust system to generate realistic 3D human avatars from single RGB images. It integrates advanced techniques in computer vision and deep learning, focusing on pose-guided normal prediction and fine-detailed implicit surface reconstruction. The system is suitable for applications in virtual reality, fashion, animation, and gaming.

---

## Key Features

- **Pose-Guided Normal Prediction**  
  Leverages SMPL body models and neural networks to estimate accurate surface normals for clothed human bodies.
  
- **Fine-Detailed Reconstruction**  
  Combines local image features and body shape priors to create detailed 3D models with intricate clothing and surface textures.
  
- **High-Quality 3D Models**  
  Capable of generating 3D meshes with high fidelity, validated on datasets like AGORA and THuman.

---

## Applications

- **Virtual Reality & Gaming**: Create lifelike avatars for immersive environments.
- **Fashion & Animation**: Design detailed 3D characters for creative industries.
- **Healthcare**: Convert medical scans (e.g., CT/MRI) into 3D anatomical models.

---

## Project Workflow

1. **Input Processing**  
   An RGB image is processed to estimate a parametric SMPL body mesh.
   
2. **Normal Map Prediction**  
   Pose-guided normal maps are generated to represent surface normals of the body.

3. **Iterative Refinement**  
   Normal maps are refined iteratively for enhanced accuracy.

4. **3D Reconstruction**  
   Combines local features with normal maps to generate fine-detailed 3D meshes.

---

## Dataset

The system was trained and evaluated on the **AGORA** and **THuman** datasets. Additional synthetic renderings were used to supplement training data.

---

# Installation

This document provides step-by-step instructions for setting up the PIFuHD system for high-resolution 3D human digitization.

## Step 1: Conda Installation

If you do not already have Conda installed, follow this [YouTube tutorial](https://www.youtube.com/watch?v=_hcYgA-UjCc) to install Conda.

## Step 2: Clone the Repository

Clone this GitHub repository using the following commands:
```bash
git clone https://github.com/facebookresearch/pifuhd
cd pifuhd
```

## Step 3: Create a Conda Environment
1) Create a new Conda environment:
   
```bash
conda create -n pifuhd python=3.6
```

3) Activate the environment:

```bash
conda activate pifuhd
```

## Step 4: Install Dependencies

### Using Conda

Install PyTorch and torchvision:
```bash
conda install -c pytorch pytorch
conda install -c pytorch torchvision
```

### Using pip
Install additional libraries:

```bash
pip install pillow
pip install json
pip install scikit-image
pip install tqdm
pip install opencv-python
pip install trimesh
pip install ffmpeg
```

### Install PyOpenGL
Download the appropriate .whl file for PyOpenGL and install it:

```bash
pip install C:/Users/user/Downloads/PyOpenGL-3.1.5-cp36-cp36m-win_amd64.whl
```

## Step 5: Setup Checkpoints

### Create a directory for storing model checkpoints:

```bash
mkdir checkpoints
```

[Link](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbWhZR253X1dtT0d5bnk0THVyY0p3aG1HeHBvZ3xBQ3Jtc0tuMkh6QXp5Q2NFZEtYclJkVmxrN0hmUkQ0T2haenFic2ZWN2ZHSjRDVHg2SnhJZGlYaVBkbFkzUFpKSlU1S2w1QVk3Z2tGdmc2OHRsN1lhQTNKWmpXaTBWTGlpVmIySEhtUUQ5Tld2LU9uaDc1eG4tNA&q=https%3A%2F%2Fdl.fbaipublicfiles.com%2Fpifuhd%2Fcheckpoints%2Fpifuhd.pt&v=zzgCoyYyuN0)

## Step 6: Run the Model

To test the setup, run the following commands:

### 1) Generate results from an input image:

```bash
python -m apps.simple_test
```

### 2) Render a turntable animation of the reconstruction:

```bash
python -m apps.render_turntable -f ./results/pifuhd_final/recon -ww 512 -hh 512
```

## Results

![1](https://github.com/user-attachments/assets/f1601c59-44f8-4bf8-907f-89ea80bd1b2b)
![Gif](https://github.com/user-attachments/assets/ec518a32-78a7-41d0-bd0f-3a224d1271e2)

![1 2d](https://github.com/user-attachments/assets/d0935ed7-5d10-4ac8-8739-b5c8c90659c6)






