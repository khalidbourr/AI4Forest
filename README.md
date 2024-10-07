# **AI4Forest: Forest Navigation Virtual Environment**

## **Project Description**

**AI4Forest** is a virtual environment created in Unreal Engine 5 (UE5) designed for training and testing robotic navigation algorithms in a realistic forest setting. The environment includes detailed terrain generated from real-world elevation data, vegetation, rocks, and other natural features to simulate the challenges a robot might face in a forested area.

## **Table of Contents**

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Installing Unreal Engine 5 on Linux](#installing-unreal-engine-5-on-linux)
- [Setting Up the Project](#setting-up-the-project)
- [Running the Project](#running-the-project)
- [Assets and Licensing](#assets-and-licensing)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## **Features**

- Realistic forest environment based on Digital Elevation Model (DEM) data.
- Detailed vegetation including trees, grass, and rocks.
- Configured for robotic navigation and traversability analysis.
- Suitable for training AI models in a simulated forest setting.

---

## **Prerequisites**

Before you begin, ensure you have the following:

- A computer running a Linux distribution (Ubuntu 20.04 LTS or later is recommended).
- At least **16 GB of RAM** (32 GB recommended for UE5 projects).
- A **dedicated GPU** with at least **6 GB of VRAM** that supports Vulkan (e.g., NVIDIA GTX 1060 or equivalent).
- **Git** installed for cloning the repository.
- **Git LFS** (Large File Storage) installed for handling large files.

---

## **Installation**

### **Installing Unreal Engine 5 on Linux**

UE5 is not officially distributed as pre-built binaries for Linux, so you'll need to build it from source. Here's how to install UE5 on Linux:

#### **1. Install Required Dependencies**

Open your terminal and install the necessary dependencies:

```bash
sudo apt update
