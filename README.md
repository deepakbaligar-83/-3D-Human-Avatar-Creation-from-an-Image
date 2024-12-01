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

## Installation

### Prerequisites

- **Operating System:** Ubuntu 18.04/20.04
- **GPU Memory:** >12GB
- **Python:** >=3.8

### Required Libraries

- PyTorch 1.13.0  
- PyTorch3D  
- CUDA 11.3  
- GCC 7.5.0  

Install the required libraries:
```bash
pip install torch torchvision
pip install pytorch3d
```

## Results

![1](https://github.com/user-attachments/assets/f1601c59-44f8-4bf8-907f-89ea80bd1b2b)
![Gif](https://github.com/user-attachments/assets/ec518a32-78a7-41d0-bd0f-3a224d1271e2)

![1 2d](https://github.com/user-attachments/assets/d0935ed7-5d10-4ac8-8739-b5c8c90659c6)






