# Email-Spam-Ham-Detection

#### In this project, we build a spam detector using 5 Machine Learning models and evaluate them with test data using different performance metrics used. The data used for this project is from the Enron email dataset which contains approximately 500,000 emails generated by employees of the Enron Corporation. It was obtained by the Federal Energy Regulatory Commission during its investigation of Enron's collapse. We have used a pre-processed version of the dataset which contains both spam and ham emails in different proportions

### Dataset Used:- The Enron Email 

Dataset Description:- This is one of the biggest email data sources in the world. Almost half a million files spread over 2.5 GB. Normally, emails are very sensitive, and rarely released to the public, but because of the shocking nature of Enron’s collapse, everything was released to the public.

## Download Dataset

Download a set of spam and ham actual emails. Each email is a separate plain text file. Unzip the compressed tar files, read the text and load it into a Pandas Dataframe. Convert the dataframe to a Pickle object.

## Clean the Dataset

we will import re in this module to check if a perticular string matches a given regular expression.The ‘sub’ in the function stands for SubString, a certain regular expression pattern is searched in the given string(3rd parameter), and upon finding the substring pattern is replaced by repl(2nd parameter), count checks and maintains the number of times this occurs. 

## Preprocess the Data

Split the text string into individual words and stem each word. 
Remove english stop words. (Stopwords are the English words which does not add much meaning to a sentence)

### Split and Stem
Split the text by white spaces and link the different forms of the same word to each other, using stemming. For example “responsiveness” and “response” have the same stem/root - “response”.

### Remove Stop Words
Some words such as “the” or “is” appear in all emails and don’t have much content to them. These words are not going to help the algorithm distinguish spam from ham. Such words are called stopwords and they can be disregarded during classification.

## Vectorize Words and Split Data to Train/Test Sets
Transform the words into a tf-idf matrix using the sklearn TfIdf transformation. Then, create train/test sets with the train_test_split function, using stratify parameter. The dataset is highly unbalanced and the stratify parameter will make a split so that the proportion of values in the sample produced will be the same as the proportion of values provided to parameter stratify. For example, if variable y is 0 and 1 and there are 30% of 0’s and 70% of 1’s, stratify=y will make sure that the random split has 30% of 0’s and 75% of 1’s.

## Train a Classifier
Trained five models using the training data:  
a.    Naive Bayes  
b.    Decision Tree  
c.    SVM  
d.    Random Forest  
e.    Logistic Regression  
    
Using the trained models, predicted the email label for test dataset. Calculated four metrics to gauge performance of the models:  
a.    Accuracy  
b.    Precision  
c.    Recall  
d.    F-score  

Below are the metrics explanation:-

**1. Precision**  
Precision refers to the closeness of two or more measurements to each other. In Machine Learning, precision is the fraction of relevant instances among the retrieved instances  
    Precision = TP / (TP + FP) (Where TP = True Positive, TN = True Negative, FP = False Positive, FN = False Negative).

**2. Accuracy**  
Accuracy refers to the closeness of a measured value to a standard or known value.  
    Accuracy = (TP+TN) / ALL

**3. Recall**    
Recall is how many of the true positives were recalled (found), i.e. how many of the correct hits were also found.  
    Recall = TP / (TP + FN)

4. F-Score  
F-scores are a statistical method for determining accuracy accounting for both precision and recall. It is essentially the harmonic mean of precision and recall.  

## Compare performance of different classifiers 

| Model Name  | Accuracy  | Precision |  Recall | F-Score |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Naive Bayes  | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| Decision Tree  | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| SVM  | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| Random Forest  | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| Logistic Regression  | Content Cell  | Content Cell  | Content Cell  | Content Cell  |

