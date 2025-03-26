# Template for Isaac Lab Projects

[![IsaacSim](https://img.shields.io/badge/IsaacSim-4.5.0-silver.svg)](https://docs.isaacsim.omniverse.nvidia.com/latest/index.html)
[![Python](https://img.shields.io/badge/python-3.10-blue.svg)](https://docs.python.org/3/whatsnew/3.10.html)
[![Linux platform](https://img.shields.io/badge/platform-linux--64-orange.svg)](https://releases.ubuntu.com/20.04/)
[![Windows platform](https://img.shields.io/badge/platform-windows--64-orange.svg)](https://www.microsoft.com/en-us/)

## Overview

This is the updated version of [Isaac Sim Project Template](https://github.com/isaac-sim/IsaacLabExtensionTemplate). This repository serves as a template for building projects or extensions based on Isaac Lab. Here I have added only two example for humanoid locomotion project of `h1` and `g1` humanoid robot.


**Key Features:**
- `Isolation` Work outside the core Isaac Lab repository, ensuring that your development efforts remain self-contained.
- `Flexibility` This template is set up to allow your code to be run as an extension in Omniverse.

**Keywords:** extension, template, isaaclab

## Installation

- Install Isaac Lab by following the [installation guide](https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/index.html). We recommend using the conda installation as it simplifies calling Python scripts from the terminal.

- Clone this repository separately from the Isaac Lab installation (i.e. outside the `IsaacLab` directory):

```bash
# Option 1: HTTPS
git clone https://github.com/isaac-sim/IsaacLabExtensionTemplate.git

# Option 2: SSH
git clone git@github.com:isaac-sim/IsaacLabExtensionTemplate.git
```

- Throughout the repository, the name `test_project` only serves as an example and we provide a script to rename all the references to it automatically:

```bash
# Enter the repository
cd IsaacLabExtensionTemplate
# Rename all occurrences of test_project (in files/directories) to your_fancy_extension_name
python scripts/rename_template.py your_fancy_extension_name
```

- Using a python interpreter that has Isaac Lab installed, install the library

```bash
python -m pip install -e source/test_project
```

- Verify that the extension is correctly installed by running the following command:

```bash
python scripts/rsl_rl/train.py --task=Template-Isaac-Velocity-Rough-Anymal-D-v0
python scripts/rsl_rl/train.py --task=Isaac-Velocity-Flat-G1-v0
python scripts/rsl_rl/train.py --task=Isaac-Velocity-Rough-G1-v0
python scripts/rsl_rl/train.py --task=Isaac-Velocity-Flat-H1-v0
python scripts/rsl_rl/train.py --task=Isaac-Velocity-Rough-H1-v0
```

- To play with the trained model

```bash
python scripts/rsl_rl/play.py --task=Isaac-Velocity-Rough-G1-Play-v0
python scripts/rsl_rl/play.py --task=Isaac-Velocity-Rough-H1-Play-v0
```


## Summery of all the steps to run this simulation
 First, install Isaac Lab and set a conda environment
 - 
 ```bash
 # 1. Go to the conda environment with the Isaac Lab
 conda activate isaacenv

 # 2. Clone this repository the project template
 git clone https://github.com/alamgirakash2000/IsaacLabStarter 

 # 3. Go to the project repository
 cd IsaacLabEntension

 # 4. Rename the project in all the occurances (sample name: test project)
 python scripts/rename_template.py test_project  

 # 5. Install the libraries
 python -m pip install -e source/test_project 

 # To verify and train an environment
 python scripts/rsl_rl/train.py --task=Isaac-Velocity-Rough-G1-v0

 # To play the trained model
 python scripts/rsl_rl/play.py --task=Isaac-Velocity-Rough-G1-Play-v0
 ```


