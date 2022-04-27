# Create a virtual environment
Prophet only runs in 

## Create a virtual environment (also view and remove) ##
in windows: type "cmd" in "Type here to search" and run it as administrator
in cmd: conda create -n py37prophet python=3.7
in cmd: conda info --envs
in cmd: conda env remove -n py37prophet

## Activate and deactivate a virtual environment ##
in cmd: conda activate py37prophet
in cmd: conda deactivate

## Check Python Version ##
in py37prophet: python --version

## Add virtual environment to Jupyter Notebook Kernel (also, view and remove) ##
in py37prophet: pip install ipykernel
in py37prophet: python -m ipykernel install --user --name=py37prophet
in cmd or py37prophet: jupyter kernelspec list
in cmd or py37prophet: jupyter kernelspec uninstall py37prophet

## Start the jupyter notebook in the virtual environment
in windows: go to the folder you want to use and type "cmd" in the address bar
in cmd: conda activate py37prophet
in py37prophet: jupyter notebook
in jupyter notebook: !python --version




# Install prophet
in windows: type "cmd" in "Type here to search" and run it as administrator
in cmd: conda activate py37prophet
in py37prophet: pip install pystan
in py37prophet: conda install -c conda-forge prophet

# Helpful sites
https://stackoverflow.com/questions/53178281/installing-fbprophet-python-on-windows-10
consider runnting the following
conda install libpython m2w64-toolchain -c msys2

