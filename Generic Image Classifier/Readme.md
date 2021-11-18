
# Generic Image Classifier Using PyTorch

In this project, I used transfer learning to re-train a pre-trained image classifier to classify flower names. **Transfer Learning** technique gives the advantage of using the efficient feature extractor architectures that is trained on very large datasets such as **COCO** and **ImageNet**. all what we need to do is replace the tail of the neural network architecture (the classifier layers) with custom layers and only train this custom layers to classify the desired images. For this purpose, we need to prepare a dataset for our classifier to train on.   
  
  ![img](https://github.com/AbdullahBahi/My-Portfolio/tree/master/Generic%20Image%20Classifier/0.png?raw=true)
  
**NOTE**  
This Project is the final project of Udacity's [AI Programming with Python Nanodegree program](https://www.udacity.com/course/ai-programming-python-nanodegree--nd089).

## Project Layout

### Part(1)-Development:
Developing an Image Classifier with Deep Learning using jupyter notebook.

### Part(2)-Command Line App:
Building a command line application using the developed image classifier

## Command Line App Specifications

The project includes two main files `train.py` and `predict.py`.  
**The first file**, `train.py`, will train a new network on a dataset and save the model as a checkpoint.  
**The second file**, `predict.py`, uses a trained network to predict the class for an input image.

### File Specifications

1. Train a new network on a dataset with `train.py`
   - **Basic usage**: `python train.py data_directory`  
   This Prints out training loss, validation loss, and validation accuracy as the network trains

   - **Options**:
	   - Set directory to save checkpoints: `python train.py data_dir --save_dir save_directory`
	   - Choose architecture: `python train.py data_dir --arch "vgg13"`
	   - Set hyperparameters: `python train.py data_dir --learning_rate 0.01 --hidden_units 512 --epochs 20`
	   - Use GPU for training: `python train.py data_dir --gpu`

2. Predict flower name from an image with `predict.py` along with the probability of that name.  
That is, we'll pass in a single image </path/to/image> and return the flower name and class probability.

   - **Basic usage**: `python predict.py </path/to/image> checkpoint`

   - **Options**:
	   - Return top KK most likely classes: `python predict.py input checkpoint --top_k 3`
	   - Use a mapping of categories to real names: `python predict.py input checkpoint --category_names cat_to_name.json`
	   - Use GPU for inference: `python predict.py input checkpoint --gpu`

## Project repository
View source code for this project from [here](https://github.com/AbdullahBahi/Generic-Image-Classifier-Using-Pytorch).