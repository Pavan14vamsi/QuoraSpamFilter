Read Me

# Project Details

## Objective
A spam filter for quora questions. The objective is to create a neural network that can reliably differentiate between spam questions and genuine ones.

## Logic
Implementing a small LSTM Neural Network to classify questions as spam (1) or not spam (0)
There is a class imbalance problem (94% -0 and 6%-1).
The first iteration with the same distribution didn't give satisfactory results, in the second attempt I took a subset of the training data so the model doesn't get too influenced by the majority class. The new balanced set has equal representation from both classes

I used the tokenizer to convert the words into integer sequences, the idea is that the embedding layer in the model can adequately learn relationships between words with "Spatial intuition".



## The model
Although I wanted a small model, after a few experiments this huge one performed adequately. I reached this networked after some trial and error. Unfortunately my pc wasn’t powerful enough to enable further experimentation.


## The Result
The roc and accuracy scores were acceptable at a glance. The output probabilities are too wide apart for the threshold to make any difference. Any further improvement will have to be made on the model architecture. Perhaps by removing some outlier questions (such as those which are too verbose). 


##  File Manifest
Quora Spam Filter.ipynb : The file that does all the work. Cleaning, preparation, building, training & testing the model

Balanced_set.csv: I saved the balanced training data so that I can resume my work.
 
train.csv: The raw data. Containing the questions.
https://drive.google.com/file/d/1dUhzH8mbJbUcdYCdltV7zjqu9rVDHRni/view?usp=sharing

QuoraSpamFilter: The folder containing the saved model in case you wish to use the model directly. 
https://drive.google.com/drive/folders/1vkCYQQn3GhylWmZebBiP1hxbWNKLaiy-?usp=sharing

QuoraSpamFilterWeights.h5 : The weights of the model.
https://drive.google.com/file/d/10IdwpUzEzVGUSbn9z_T1bDcmP4vWxfxS/view?usp=sharing




# Packages Used
Numpy==1.18.5 (Later versions seem to have some problem with tensorflow)
Tensorflow==2.3.0
nltk==3.6.2
sklearn==0.6.2
Pandas==1.2.4



#Copyright and License
Free for anyone to use, however they like. Just cite me if you do.
