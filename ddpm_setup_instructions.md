
# Diffusion Model Setup and Execution

This repository provides instructions to set up the environment and run the code for your Diffusion Model using Python

---

## Environment Setup  

### Step 1: Create a Conda Environment  
Run the following command to create a new Conda environment named `ddpm` with Python 3.12:  
```
conda create -n ddpm python=3.12
```

### Step 2: Activate the Environment  
Activate the newly created environment:  
```
conda activate ddpm
```

### Step 3: Install PyTorch with CUDA Support  
Install the specific versions of PyTorch, Torchvision, and Torchaudio with CUDA 11.8 support:  
```
pip install torch==2.5.0 torchvision==0.20.0 torchaudio==2.5.0 --index-url https://download.pytorch.org/whl/cu118
```

### Step 4: Install Additional Dependencies  
Install OpenCV, TQDM, and Matplotlib using Conda:  
```
conda install opencv tqdm matplotlib -c conda-forge
```

---

## Running the Code  

To execute the code, submit the `job.sh` script using the `qsub` command:  
```
qsub job.sh
```

---

## Notes  
1. **CUDA Compatibility**: Ensure your system's GPU drivers are compatible with CUDA 11.8.
2. **Error Debugging**: If any packages fail to install or execute, verify the Python version and package sources. Use `conda list` to confirm installed packages.
3. **Environment Management**: To delete the environment when it's no longer needed:  
   ```
   conda remove --name ddpm --all
   ```

---

