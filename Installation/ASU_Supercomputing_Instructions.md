**ASU Supercomputing Instructions**

https://asurc.atlassian.net/wiki/spaces/KESC/pages/1914667538/Managing+Python+Modules+Through+the+Mamba+Environment+Manager

From shell, enter:  interactive 

module load mamba/latest

copy from github: git clone https://github.com/pyg-team/pytorch_geometric.git 

                                 cd   

                                 pip install -e .

mamba create --name <new_environment_name> --clone <environment_to_copy>
This will create an environment called <new_environment_name> that is copied from <environment_to_copy>.

mamba create -n  yourENVname

source activate yourENVname

source deactivate 

mamba info --envs   

remove env:  rm -r  /home/hwang49/.conda/envs/xxx

remove env in Juputer:  rm -r   /home/hwang49/.local/share/jupyter/kernels/xxx

mkjupy xxx

mamba install -c conda-forge pandas

mamba install -c conda-forge  pytorch torchvision torchaudio

mamba install -c conda-forge qiskit=1.0.1

mamba install -c conda-forge qiskit-algorithms=0.3.0

mamba install -c conda-forge qiskit-machine-learning=0.7.2

mamba install -c conda-forge qiskit-aer

mamba install -c conda-forge -c pytorch -c nvidia pytorch-gpu torchvision torchaudio pytorch-cuda=12

mamba install -c conda-forge -c pytorch  pytorch torchvision torchaudio
