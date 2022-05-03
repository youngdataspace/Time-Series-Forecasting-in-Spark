<img src = "https://github.com/youngdataspace/Time-Series-Forecasting-in-Spark/blob/main/Intro.gif?raw=true" width=80% height=80%>

# 1. Introduction
In this post, we will explore scalable time-series forecasting in PySpark. We will build time-series models using Convolutional Neural Network (CNN), Long Short-Term Memory, Facebook Prophet, and Seasonal ARIMA. We will then train 500 time-series Prophet models in parallel with PySpark in Google Colab. I am going to break down each step in detail, from installing packages to evaluating the models.

Let's get started!

This repository contains all the codes necessary to replicate the contents in <a href = "https://medium.com/@y.s.yoon/scalable-time-series-forecasting-in-spark-prophet-cnn-lstm-and-sarima-a5306153711e">this blog post</a>. If you have any comments or suggestions, email me at y.s.yoon@berkeley.edu.

# 2. Create a Virtual Environment
Prophet only runs in Python 3.8 or a lower version. For those of us who use a higher version like myself, we can create a virtual environment and use a lower version. I've listed the detailed steps to create a virtual environment with Python 3.7.

### 2.1. Create and view virtual environments
- in Windows: type "cmd" in "Type here to search" and right-click the "Command Prompt" to run it as administrator
- in cmd: conda create -n py37prophet python=3.7
- in cmd: conda info --envs

FYI, we can remove the virtual environment with the following command but don't run it now.
- in cmd: conda env remove -n py37prophet

### 2.2. Activate the virtual environment
- in cmd: conda activate py37prophet

FYI, we can deactivate the virtual environment with the following command but don't run it now.
- in cmd: conda deactivate

### 2.3. Check the Python's Version
Make sure you have Python 3.7 installed.
- in py37prophet: python --version

### 2.4. Add the virtual environment to Jupyter Notebook's list of Kernels
- in py37prophet: pip install ipykernel
- in py37prophet: python -m ipykernel install --user --name=py37prophet
- in cmd or py37prophet: jupyter kernelspec list

FYI, we can remove it with the following command but don't run it now.
- in cmd or py37prophet: jupyter kernelspec uninstall py37prophet

### 2.5. Start Jupyter Notebook in the virtual environment
- in windows: In File Explorer, go to the folder you want to use and type "cmd" in the address bar
- in cmd: conda activate py37prophet
- in py37prophet: jupyter notebook
- in jupyter notebook: !python --version # To check the python version

# 3. Install Prophet and Other Useful Packages
### 3.1. Install Prophet
Installing Facebook Prophet can be a headache. Make sure you have Python 3.8 or lower and follow the below instructions.
- in windows: type "cmd" in "Type here to search" and run it as administrator
- in cmd: conda activate py37prophet
- in py37prophet: pip install pystan
- in py37prophet: conda install -c conda-forge prophet

<a href = "https://stackoverflow.com/questions/53178281/installing-fbprophet-python-on-windows-10">This post</a> was very helpful for me.

### 3.2. Prophet asks us to install/update the following (not an absolute must)
- pip install plotly
- pip install jupyter
- pip install ipywidgets

# 4. Implementation of Demand Forecasting in Python
Follow along in "CNN_LSTM_Prophet_SARIMA_Models.ipynb".

# 5. Implementation of Scalable Demand Forecasting with PySpark in Google Colab
Follow along in "Time_Series_at_Scale_with_Spark.ipynb".
