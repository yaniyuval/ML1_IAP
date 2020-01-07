

# Hands on Python Machine Learning - IAP at MIT 
This IAP is aimed to give you practical machine learning skills. Every session will be devided to a teaching session (that will be done with jupyter notebooks - lesson*.ipynb) and a practice session where you will try code things that we learn (basically using machine learning to get predictions for some data set).  

The main topics of the sessions are:
- Classification with Random Forest
- Regression with Random forest and XGBoost
- Fully connected Neural Networks (using pytorch)
- Convolutional Neural Networks

If we will successfully finish on time the first four sessions,  the fifth session will deal with transfer learning (or we will complete topics from the first four sessions). 

## Getting Started
The easiest option to get the course material is cloning this git repository.
To do so type git clone
In order to get all the material for the course I suggest cloning this git repository. To do so type:
```
git clone https://github.com/yaniyuval/ML_IAP.git
``` 

Alternatively, you can download a zip file.


### Prerequisites
### Installing
#### Installing anaconda:
To install Anaconda please follow the instructions [here](https://docs.anaconda.com/anaconda/install/), since the installation depends on the OS you have, I cannot provide the exact way how you will install it. 

After you downloaded anaconda, please update your conda version before continuing with these instructions.
This is done  by typing 

```
conda update --all
```
If you do not want to update all your packages - please read [here](https://www.anaconda.com/keeping-anaconda-date/) about other options how to do partial update (not recommended unless you know what you are doing).

#### Updating python version
I am using Python 3.7.5, and I encourage you to update your python version to be at least 3.6.
You can do this using anaconda:
'''
conda update python
'''

#### Virtual environment
To create a new virtual environment called ML_IAP with anaconda type:

```
conda create --name ML_IAP python=3.7.5
```
If you want to use a different python version you can change the python version but take into account that I verified that the code in the notebooks runs with this version (I certainly do not recommend any version prior to 3.6). 

To activate the environment (you should do this always before opening the course notebooks or when installing packages):
```
conda activate ML_IAP
```

#### Installing packages
Here you will install packages that are necesary for the course. Please type:

```
conda install scikit-learn numpy matplotlib scipy IPython pandas
```
also type the following commands:
```
conda install jupyter notebook
```

```
pip install category_encoders
```
If you have any problems with category_encoders package, try typing:
```
conda install -c conda-forge category_encoders
```

Continue by typing
```
pip install xgboost
```

```
pip install pandas_summary
```
If you want to understand what is a virtual environmnet please read [here](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/).

If you want more details regarding creating virtual environments, please read [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)


### Installing pytorch
pytorch is the package we will use for deep learning. The specific line of code you will run in order to get pytorch, depends on your OS and your python version. 
In order to understand what should you type, please go [here](https://pytorch.org/get-started/locally/) and choose your OS/versions. 
I installed a version without a GPU (choosing CUDA none) and needed to type:

```
conda install pytorch torchvision -c pytorch
```
But this is only on my machine.
Note that even if you do have a GPU (which is great!) I will not teach anything that requires it, and all the code was written to run on a CPU.

Since there is a new release of pytorch which has some problems, I recommend you to type:
```
pip install "pillow<7"
```
Although this might be solved in the next few days - see [here](https://github.com/pytorch/vision/issues/1712)

#### Installing fastai
type
```
 pip install fastai
```
if you have problems in installing fastai - please read [here](https://docs.fast.ai/install.html)




#### Runinng Jupyter notebook
Go to the IAP library (where you cloned the course repository) and type (don't forget to first activate your ML_IAP virtual environment):
```
jupyter notebook
```

Now choose a notebook that you want to run.

#### Comment - Jupyter Notebooks
All through the IAP, we will use Jupyter notebooks. If you are not familiar with Jupyter notebooks, please go over some basic tutorial (e.g., [fastai tutorial notebook](https://github.com/fastai/course-v3/blob/master/nbs/dl1/00_notebook_tutorial.ipynb), [general introduction to jupyter notebooks](https://realpython.com/jupyter-notebook-introduction/))  and make sure you are able to run code on notebooks. I also added to the repository a tutorial notebook (jupyter-intro_RASP.ipynb) which is taken from [Stephan's Rasp repository](https://github.com/raspstephan/MPI-ML-Tutorial/blob/master/jupyter-intro.ipynb).

### Test packages
to test that your installation of all packages has worked you can run that you can run the single cell in the notebook test_packages.ipynb.

If you get some error, please try to undersand which package you did not install properly and try to reinstall it. 

#### Please let me know if you have problems: yaniyuval@gmail.com
