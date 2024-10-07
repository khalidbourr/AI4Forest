# **AI4Forest: Forest Navigation Virtual Environment**

## **Project Description**

**AI4Forest** is a virtual environment created in Unreal Engine 5 (UE5) designed for training and testing robotic navigation algorithms in a realistic forest setting. The environment includes detailed terrain generated from real-world elevation data, vegetation, rocks, and other natural features to simulate the challenges a robot might face in a forested area.


![Alt text](/Screenshot%20from%202024-10-07%2014-04-27.png) "3D realistic Forest")

## **Table of Contents**

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Installing Unreal Engine 5 on Linux](#installing-unreal-engine-5-on-linux)
- [Setting Up the Project](#setting-up-the-project)
- [Running the Project](#running-the-project)


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
sudo apt install build-essential clang lld cmake python3-dev libvulkan1 libvulkan-dev vulkan-tools
```


#### **2. Install Additional Dependencies**

For Ubuntu 22.04 and later:

```bash

sudo apt install libxcb-xinerama0 libxcb-xinput0
```

#### **3. Install Git and Git LFS**

If you haven't already:

```bash

sudo apt install git git-lfs
git lfs install

```

#### **4. Clone the Unreal Engine 5 Repository**

##### **Getting Access to Unreal Engine 5 Source Code**

To build Unreal Engine 5 from source, you'll need access to the UE5 repository on GitHub provided by Epic Games. Follow these steps to gain access:

##### **Sign Up for an Epic Games Account**

1. Go to the [Epic Games website](https://www.epicgames.com/id/register) and create an account, or log in if you already have one.

##### **Associate Your GitHub Account with Epic Games**

1. Log in to the [Epic Games Developer Portal](https://www.unrealengine.com/en-US/ue-on-github).
2. Follow the instructions to link your GitHub account to Epic Games.

##### **Accept the EULA**

1. After linking your GitHub account, you will receive an invitation to join the `EpicGames` organization on GitHub.
2. Accept the invitation to gain access to the Unreal Engine repositories.

##### **Clone the UE5 Repository**

Once you have access to the repository, you can clone it by running the following command in your terminal:

```bash
git clone https://github.com/EpicGames/UnrealEngine.git ~/UnrealEngine
```

#### **5. Build Unreal Engine 5**

Navigate to the UE5 directory and run the setup scripts:

```bash

cd ~/UnrealEngine
./Setup.sh
./GenerateProjectFiles.sh
make

```
    Note: The make command will take several hours, depending on your hardware.

#### **6. Verify the Installation**

After the build completes, you can test the editor:

```bash

cd ~/UnrealEngine/Engine/Binaries/Linux
./UnrealEditor

```

or (for better performance)

```bash
./UnrealEditor -vulkan
```

If the editor launches, you've successfully installed UE5 on Linux.

#### **6. Setting Up the Project**
1. Clone the AI4Forest Repository

Navigate to the directory where you want to store the project and clone it using SSH:

```bash

git clone git@github.com:khalidbourr/AI4Forest.git

```

    Note: Ensure you have SSH access set up for GitHub.

2. Install Git LFS and Pull Large Files

If you haven't installed Git LFS:

```bash


sudo apt install git-lfs
git lfs install

```

Pull the LFS files:

```bash

git lfs pull
```

3. Verify the Project Files

Ensure that all project files, including .uasset and .umap files, are present.
Running the Project
1. Open Unreal Engine Editor

Launch UE5:

```bash

cd ~/UnrealEngine/Engine/Binaries/Linux
./UnrealEditor
```

or (for better performance)

```bash
./UnrealEditor -vulkan
```

2. Open the AI4Forest Project

    In the Unreal Editor, click on "Browse" and navigate to the cloned AI4FOREST project directory.
    Select the AI4FOREST.uproject file and open it.

3. Wait for Asset Compilation

The first time you open the project, UE5 may need to compile shaders and load assets. This can take some time.
4. Explore the Environment

  Go to File --> Open Level --> Landscape 
  
  Use the viewport to navigate around the forest environment.
  Play the scene by clicking on the "Play" button to test any interactive elements.
