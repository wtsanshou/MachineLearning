# Machine Leaning project using Python

## Objective
1. Follow the <a href="http://machinelearningmastery.com/machine-learning-in-python-step-by-step/">demo</a>
2. Install machine learning envirnment
3. Have a first view of a machine learning project

## Prerequistites

* OS: Ubuntu 16.04
* Pythone: 2.7.12

## Setup Envirnment

### Install Pythone
```bash
sudo apt-get update
sudo apt-get install python
```

### Installing the SciPy Stack

* Installing via pip
```bash
sudo apt-get install -y python-pip
sudo -H pip install --upgrade pip

pip install --user numpy scipy matplotlib ipython jupyter pandas sympy nose

sudo pip install -U scikit-learn

sudo apt-get install python-tk

sudo su
## put export PATH=$PATH:/home/<your_user>/.local/bin
## into ~/.bashrc

source ~/.bashrc
```

### Check Libraries version

Write a python script `versionCheck.py`
```
# Check the versions of libraries

# Python version
import sys
print('Python: {}'.format(sys.version))
# scipy
import scipy
print('scipy: {}'.format(scipy.__version__))
# numpy
import numpy
print('numpy: {}'.format(numpy.__version__))
# matplotlib
import matplotlib
print('matplotlib: {}'.format(matplotlib.__version__))
# pandas
import pandas
print('pandas: {}'.format(pandas.__version__))
# scikit-learn
import sklearn
print('sklearn: {}'.format(sklearn.__version__))
```
 
run
```bash
python versionCheck.py
```

Should see result like:
```
Python: 2.7.12 (default, Nov 19 2016, 06:48:10) 
[GCC 5.4.0 20160609]
scipy: 0.19.0
numpy: 1.13.0
matplotlib: 2.0.2
pandas: 0.20.2
sklearn: 0.18.1
```

## Load the Data
We are going to use the iris flowers dataset. This dataset is famous because it is used as the “hello world” dataset in machine learning and statistics by pretty much everyone.

The dataset contains 150 observations of iris flowers. There are four columns of measurements of the flowers in centimeters. The fifth column is the species of the flower observed. All observed flowers belong to one of three species.

* Import libraries
write python script `loadLibraries.py`
```
# Load libraries
import pandas
from pandas.tools.plotting import scatter_matrix
import matplotlib.pyplot as plt
from sklearn import model_selection
from sklearn.metrics import classification_report
from sklearn.metrics import confusion_matrix
from sklearn.metrics import accuracy_score
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
from sklearn.naive_bayes import GaussianNB
from sklearn.svm import SVC
```

* Load Dataset

write python script `loadDataset.py`
```
# Load dataset
url = "https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data"
names = ['sepal-length', 'sepal-width', 'petal-length', 'petal-width', 'class']
dataset = pandas.read_csv(url, names=names)

# shape
print(dataset.shape)

# head
print(dataset.head(20))

print()

# descriptions
print(dataset.describe())

print()

# class distribution
print(dataset.groupby('class').size())

```