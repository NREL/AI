# Notes for Running Jupyter Notebooks on HPC

Some general notes for running jupyter notebooks on HPC (such as kestrel).

## NREL Kestrel notes

Follow these steps:

1) Log into kestrel: username@kestrel.hpc.nrel.gov
2) Ensure you have a working Conda distribution.
    - Install the conda environment for either TensorFlow or PyTorch:
    - Create a new conda environment using the environment file: 
        
        `conda env create --prefix /scratch/<username>/.conda-envs --file hyperparameter_tuning_pt.yml`.

    - To update:
        
        `conda env update --name hyperparameter-tuning-pt --file hyperparameter_tuning_pt.yml --prune` 
    

    - Activate the new environment: `conda activate hyperparameter-tuning-pt`.
    
3) Request interactive node:
    - `salloc -A <allocation> --partition=gpu-h100 --time 24:00:00 --gpus=4 --exclusive --mem=0`
    - `module load conda`
    - `conda activate /scratch/<username>/.conda-envs/hyperparameter-tuning-pt`
4) Launch the jupyter notebook instance:
    - `jupyter-notebook --no-browser --ip=$(hostname -s)`
5) On personal computer ssh into the remote session with:
    - `ssh -N -L 8888:<node_name>:8888 <user_name>@kestrel.hpc.nrel.gov`
6) Copy the URL from the interactive node and paste into a browser window. It will look something like:
    - `http://127.0.0.1:8888/?token=<alphabet_soup>`