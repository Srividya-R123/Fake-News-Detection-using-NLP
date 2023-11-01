# FAKE NEWS DETECTION USING NLP 


## DATASET USED:  
 	https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset 
  
  Two datasets are used, one for true news and other for fake news.  

## LIBRARIES USED:

For going on with our project we use and therefore import the following libraries.
* TensorFlow
* Pandas
* NumPy
* Matplotlib.pyplot
* Seaborn
* NLTK
* Regular Expressions (re)

## STEPS IMPLEMENTED:
### IMPORTING LIBRARIES
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/e408ec9d-b965-4522-bc9a-4c628737123f)

### LOADING THE DATASET
 
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/a709c6e0-e3db-44e1-bb64-5e9255ae6646)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/53bf2dd5-e99c-45ff-a4bc-f35af0a77dae)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/18e748de-ca4f-4683-89bf-1d6c7a4299ec)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/61546aa4-c76c-4e00-ac2d-8bf9e9197718)

  
### PREPROCESSING:
Preprocessing is essential to clean and prepare your text data for modeling. Common preprocessing steps include:
* Removing punctuation: This helps in normalizing the text and reducing dimensionality.
* Converting to lowercase: Ensures uniformity in text data.
* Lemmatization/Stemming: Reduces words to their base forms, e.g., "running" to "run," to handle variations of words.
* Removing stop words: Common words (e.g., "the," "and") that don't carry much information are removed.
In EDA ,  we remove the unwanted columns and merge both the true and fake news dataset into a single dataframe and add a target class column to indicate whether the news is real or fake.

### REMOVING NULL VALUES:
(from the information above there is no null values so nothing is removed)
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/09e2112a-cd04-4b1c-a94e-9a86360a876f)

### CONVERTING ALL STRINGS TO LOWERCASE:
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/bfeffb6e-3efd-45c4-a7af-55e4c23ceea8)

### REMOVE SPECIAL CHARACTER, EXTRA SPACES AND ESCAPE CHARACTER
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/2566ee6e-fc33-4893-b599-9b5592d6885f)

### REMOVING STOP WORDS 
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/0fc3826b-d420-4064-9750-9cccd6144737)

### TOKENIZATION:
 

 ### LEMMATIZATION:
 
### CREATE SENTENCES TO GET CLEAN TEXT AS INPUT FOR VECTORS
 

### PLOTTING THE WORDCLOUD FOR CLEAN TEXT
 
 
### PLOTTING THE NUMBER OF SAMPLES IN ‘SUBJECT’
 

### PREPARE DATA FOR THE MODEL. CONVERT LABEL INTO BINARY
 
### SPLIT THE DATASET  
### FEATURE EXTRACTION
(words to vectors)
Count vectorizer which considers the frequency of occurrence of a word across the corpus.
  
TF-IDF : Term Frequency - Inverse Document Frequency
The term frequency is the number of times a term occurs in a document. Inverse document frequency is an inverse function of the number of documents in which that a given word occurs.
 The product of these two terms gives tf-idf weight for a word in the corpus.
  
 
### CREATE WORD EMBEDDINGS WITH GLOVE FILE:   
### LOADING THE PRETRAINED WORD VECTORS
 
 
### CONVERT STRING INTO INTEGERS

 
### CREATE WORD-TO-INTEGER MAPPING
 
 ### EMBEDDING MATRIX  
  ### EMBEDDING LAYER
 
  ### CREATE AN LSTM NETWORK WITH A SINGLE LSTM
  
  
 ### TRAIN THE MODEL
 
 

  ### ACCURACY
  
 
 
 ### PREDICTION
 
 
 ### CONFUSION MATRIX
 
 

 ### CLASSIFICATION REPORT
 
 
 ### ROC AUC PLOT 
 







 ### MODEL PREDICTION
  
 
 ### PREDICT TEXT AND TOKENIZED
 
 ### PREDICTION OF THE MODEL
 
 


