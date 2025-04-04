# srcnn-fluid-dynamics
This repo contains the code for the implementation of Super Resolution CNN for fluid dynamics. Fluid dynamics simulations are computationally expensive and require significant storage. To address these challenges, we use deep learning techniques to reconstruct high-fidelity simulations from coarse-grained data. 

My primary responsibility in this project was implementing spatial super-resolution using the Super-Resolution Convolutional Neural Network (SRCNN). The goal was to enhance the spatial resolution of low-resolution simulation data, enabling efficient compression and reconstruction of fluid dynamics simulations.

## Spatial Super-Resolution with SRCNN

The SRCNN model takes low-resolution fluid dynamics data as input and reconstructs high-resolution data. This approach is inspired by image super-resolution techniques and adapted for physical simulation data. We also implemented a modified version of SRCNN with additional layers and improved performance.

### Key Features:
- **SRCNN Architecture**: A convolutional neural network designed for super-resolution tasks.
- **Modified SRCNN**: An enhanced version of SRCNN with additional layers and improved reconstruction accuracy.
- **Loss Function**: Mean Squared Error (MSE) is used to compare the reconstructed data with the ground truth.

## Setup Python Environment

Create a virtual environment if needed:
```
# Create a new conda environment
conda create -n srcnn-fluid python=3.7
conda activate pix2pixdental
```

Install the required dependencies:
```
pip install -r requirements.txt
```

## Running the Experiments

Place the low-resolution and high-resolution simulation data in the `data/` directory. Train the SRCNN model with proper flags (use `--help` to see all the flags and their definations), and output the high-res images.
```
python train.py
python output_pics.py
```
