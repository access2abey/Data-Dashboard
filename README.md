# Data-Dashboard


## Table of Contents
1. [Installation](https://github.com/A-Nuru/Image-Classifier#Installation)
2. [Project Motivation](https://github.com/A-Nuru/Image-Classifier#Project-Motivation)
3. [File Descriptions](https://github.com/A-Nuru/Image-Classifier#File-Descriptions)
4. [Instructions](https://github.com/A-Nuru/Image-Classifier#Instructions)
5. [Results](https://github.com/A-Nuru/Image-Classifier#Results)
6. [Licensing](https://github.com/A-Nuru/Image-Classifier#Licensing)

## Installation
The libraries employed in this project to run the code are Anaconda distribution of Python 3.*, Numpy, Pandas, Bootsrap, Plotly
## Project Motivation
This project is aimed at deploying a Data Dashboard involving writing Python code that reads in data, cleans the data, and then uses the data to make Plotly visualizations

## File Descriptions
The files associated with this work  are contained in the web_app folder which includes
* The data folder 
* The worldbankapp folder
* The wrangling_scripts folder containing the codes used to clean the data
* The Procfile
* The worldbank.py file which runs on command line

## Instructions 
While working with command line:
1. Train a new network on a data set with train.py

* Basic usage: ```python train.py data_directory```
* Prints out training loss, validation loss, and validation accuracy as the network trains
* Options:
    - Set directory to save checkpoints: ```python train.py data_dir --save_dir save_directory```
    - Choose architecture: ```python train.py data_dir --arch "vgg13"```
    - Set hyperparameters: ```python train.py data_dir --learning_rate 0.01 --hidden_units 512 --epochs 20```
    - Use GPU for training: ```python train.py data_dir --gpu```
2. Predict flower name from an image with predict.py along with the probability of that name. That is, you'll pass in a single image /path/to/image and return the flower name and class probability.

* Basic usage: ```python predict.py /path/to/image checkpoint```
* Options:
    - Return top KK most likely classes: ```python predict.py input checkpoint --top_k 3```
    - Use a mapping of categories to real names: ```python predict.py input checkpoint --category_names cat_to_name.json```
    - Use GPU for inference: ```python predict.py input checkpoint --gpu```
The best way to get the command line input into the scripts is with the argparse module in the standard library.
## Results
An application which outputs the name of a flower image fed into it is produced. Checkout the ipynb file [here.](https://github.com/A-Nuru/Image-Classifier/blob/master/Image%20Classifier%20Project.ipynb)

## Licensing
The license of this project can be found [here.](https://github.com/A-Nuru/Image-Classifier/blob/master/LICENSE)

