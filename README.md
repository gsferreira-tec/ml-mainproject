## README
This repository contains the Jupyter notebook and dataset used for the main project.

IMPORTANT: Keep the `project/data/` paths and directory structure unchanged unless you adapt the notebook paths.

### Prerequisites
- Recommended Python: 3.10 - 3.12 (use Python 3.10+). Using a virtual environment is strongly recommended.
- System packages: `git`, `python3`, and optionally `nodejs` & `npm` for notebook integrations.

### Python dependencies
The main Python packages used by the notebook include:

- numpy
- pandas
- matplotlib
- Pillow (PIL)
- scikit-learn
- tensorflow (or tensorflow-cpu if you don't plan to use a GPU)
- jupyter / ipykernel

You can install dependencies using pip from the included `requirements.txt` file:

```bash
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

Or, if you prefer conda:

```bash
conda create -n mlproj python=3.10 -y
conda activate mlproj
pip install --upgrade pip
pip install -r requirements.txt
```

Note on GPU support: If you have a compatible GPU, install the GPU-enabled build of TensorFlow appropriate for your platform. Example for Linux:

```bash
# For CPU-only, pip install 'tensorflow' will usually install the CPU build; to explicitly use CPU-only: pip install tensorflow-cpu
# For GPU: pip install tensorflow  # + additional NVIDIA drivers/CUDA/cuDNN as required
```

### Running the notebook
1. Make sure the virtual environment is active and dependencies are installed.
2. Launch Jupyter:
   ```bash
   jupyter notebook project/main_project.ipynb
   ```

### Notes
- The `project/data/` image files are large and ignored by `.gitignore` to keep the repository small; only the metadata CSVs may be tracked.
- If you run into errors related to package versions, please share your Python version and the error and we'll help pick proper versions for your setup.

If you'd like I can also add a minimal `Makefile` or other helper scripts for creating environments and running the notebook automatically.
