## Introduction
This repository is created for the example custom plot scripts of the MindAmp GUI.

## Custom plot in the GUI
To define a proper custom plot script for the GUI, serveral criteria must be fulfilled.

1. A class called ```Custom``` is required to store all the attributes and methods
2. In the ```__init__ ```method of ```Custom```, attribute ```params``` must be included to configure the plot
    - ```params``` must have the Python dict type
    - 'graph_type', 'buffer_size' and 'update_interval' are required keys   in ```params```
3. All other one-off setup procedures for the plot should be added to the ```__init__``` method. E.g. Loading a model for signal classification
4. The ```Custom``` class must include the ```custom_func``` method to receive the device signal and return data for the plot

The GUI has included common Python libraries such as NumPy, SciPy and scikit-learn for data processing. The full list of the included package can be found in the 'environment.yml' file in this GitHub repository. The custom plot scripts can involve these libraries. If users want to use their custom model in the custom plots, they may create a conda environment with the configuration file in the GitHub repository to ensure there is no package version conflict. The steps of creating such an environment are list below.

## Environment setup (Windows, macOS)
1. Download the repository with ```git clone https://github.com/MindAmp-Limited/custom_plots.git```
2. Move to the directory with ```cd custom_plots```
3. Create the conda environment and install the dependencies with 
```conda env create --name MindAmp_GUI_custom -f environment.yml```
4. Activate the environment with ```conda activate MindAmp_GUI_custom```


## Run example custom plots
1. Click the 'custom plot' button to open the custom plot window
2. Import the python scripts from the 'examples' folder
