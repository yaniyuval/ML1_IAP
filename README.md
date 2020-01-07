

# Hands on Python Machine Learning - IAP at MIT 
In this short IAP I will try to cover few algorithms and concepts that are used repeatedly in practical supervised learning.  I hope that taking this IAP will allow you to easily use basic ML, and in case you want to deepen your understanding, your knowledge you will hopefully gain in this IAP will facilitate your future learning.

Machine learning is a very broad field and naturally I will not be able to cover many aspects/topics/practices of ML. 
But the good news is that in practice there are two main techniques that are the most successful ones when applied to many different data sets:
 
- Decision tree based models (i.e. Random Forests and Gradient Boosting Machines), succesful mainly for structured data (tabular data)
- Neural networks, succesful mainly for unstructured data (such as audio, vision, and natural language), although recently also becoming popular in tabular data (see [fastai courses](https://course.fast.ai/)). 

Most of other algorithms (that gained popularity at some point during their lifetime), are outdated and are not very useful in most cases. 

In this course I will not invest a lot of time on rigorous derivations, proofs, lemma and etc... I hope that instead we will use our time to gain some intuition how ML models work and make our hands ''dirty'' with coding. This is very different from a typical academic course, which are usually very rigorous and invest their time explaining in details every aspect of the material. In the book Making Learning Whole, Harvard Professor David Perkins,  uses baseball as an analogy. We don't require kids to memorize all the rules of baseball and understand all the technical details before we let them play the game. Rather, they start playing with a just general sense of it, and then gradually learn more rules/details as time goes on. 

Every session will be devided to a teaching session (that will be done with jupyter notebooks - lesson*.ipynb) and a practice session where you will try code things that we learn (basically using machine learning to get predictions for some data set).  

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
git clone https://github.com/yaniyuval/ML1_IAP.git
``` 

Alternatively, you can download a zip file.


### Prerequisites
### Installing
#### Installing anaconda:
To install Anaconda please follow the instructions [here](https://docs.anaconda.com/anaconda/install/), since the installation depends on the OS you have, I cannot provide the exact way how you will install it. 

After you installed anaconda, please update your conda version before continuing with these instructions.
This is done  by typing 

```
conda update --all
```
If you do not want to update all your packages - please read [here](https://www.anaconda.com/keeping-anaconda-date/) about other options how to do partial update (not recommended unless you know what you are doing).

#### Updating python version
I am using Python 3.7.5, and I encourage you to update your python version to be at least 3.6.
You can update to the latest python version by typing:
```
conda update python
```

#### Virtual environment
To create a new virtual environment called ML_IAP with anaconda type:

```
conda create --name ML_IAP python=3.7.5
```
If you want to use a different python version you can change the python version but take into account that I verified that the code in the notebooks runs with this version (I certainly do not recommend any version prior to 3.6). 

To activate the environment (you should do this always before opening the course notebooks or when installing packages) type:
```
conda activate ML_IAP
```

#### Installing packages
Here you will install packages that are necessary for the course. Please type:

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

Since there is a new release of pytorch which has some problems (which should be solved in a couple of days), I recommend you to type:
```
pip install "pillow<7"
```
Although this might be solved in the next few days - see [here](https://github.com/pytorch/vision/issues/1712) and might be not necessary. 

#### Installing fastai
type:
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

If you get some error, please try to understand which package you did not install properly and try to reinstall it. 

## Recommended reading

There are numerous data sources to learn ML. During this course I tried to put links to sources that I took content from, and that I find useful. Two amazing sources of knowledge, that I repeatedly use during the IAP are:

- Python Machine Learning ([book by Sebastian Rascha](https://sebastianraschka.com)). Go to this book when you want to learn about basic concepts of ML.
- Fast.ai courses ([1](https://course.fast.ai/), [2](https://course18.fast.ai/lessonsml1/lesson1.html)) given by Jeremy Howard which is a world-class ML practitioner. Take these course if you want the newest and best ML techniques available. Also see initial version of the [book](https://mlbook.explained.ai/) Jeremy Howard is writing.

If you are interested in a basic soft intro to ML - Andrew Ng [course](https://www.coursera.org/learn/machine-learning) at coursera is a good starting point.

#### Please let me know if you have problems: yaniyuval@gmail.com
