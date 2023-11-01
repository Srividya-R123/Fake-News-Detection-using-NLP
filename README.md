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
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/8c31788b-c9e0-472d-bf30-b0b01f614c58)

 ### LEMMATIZATION:
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/adc3c14e-fac8-42aa-8414-1be9749b11fb)

### CREATE SENTENCES TO GET CLEAN TEXT AS INPUT FOR VECTORS
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/da6bb06c-2b29-44df-9324-5a1ce874ee3a)

### PLOTTING THE WORDCLOUD FOR CLEAN TEXT
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/ecd60bbf-92fa-4889-acbb-bc084cfe9125)

 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/a40d071b-5729-4889-be45-9b214a0e59b6)

### PLOTTING THE NUMBER OF SAMPLES IN ‘SUBJECT’
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/1837ce65-6d84-4b7b-bfa0-c3f1ff35410d)

### PREPARE DATA FOR THE MODEL. CONVERT LABEL INTO BINARY
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/7685ac29-6e3f-46dd-af7c-3f898d19ba26)

### SPLIT THE DATASET  
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/2d6e6da7-01f5-4d9a-82cc-a8ed7db14279)

### FEATURE EXTRACTION
(words to vectors)
Count vectorizer which considers the frequency of occurrence of a word across the corpus.
  ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/0c4c4ca7-7a6e-4faa-be3b-beeafb2e740e)

TF-IDF : Term Frequency - Inverse Document Frequency
The term frequency is the number of times a term occurs in a document. Inverse document frequency is an inverse function of the number of documents in which that a given word occurs.
 The product of these two terms gives tf-idf weight for a word in the corpus.
  ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/3f8f7772-784e-489e-bd2a-3a25fe19e743)
 
### CREATE WORD EMBEDDINGS WITH GLOVE FILE: 
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/e09e74a1-4633-4502-b4ee-36aaa664a7ea)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/848e76aa-0147-4d0a-ae08-4e396795a2b0)

### LOADING THE PRETRAINED WORD VECTORS
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/23d4459b-a6ee-4816-925d-17ce4283e56d)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/d4670a88-16bd-499b-babf-9f6b06d313ce)
 
### CONVERT STRING INTO INTEGERS
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/f02ba5bf-a031-43c1-b907-f0cd414185ba)
 
### CREATE WORD-TO-INTEGER MAPPING
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/dadc52f6-8a4c-4669-b73f-d566472ff41d)

### EMBEDDING MATRIX 
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/300e7636-b7e2-4c8b-88bd-6356d83e42ea)

### EMBEDDING LAYER
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/70c40810-1035-447d-962f-a4959a0fa42e)

### CREATE AN LSTM NETWORK WITH A SINGLE LSTM
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/06f1ead2-f577-402a-bd0c-164ee37fdd0e)
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/013a4413-0b14-4983-902b-119f60d76119)
  
### TRAIN THE MODEL
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/cef4af51-b741-4dee-a01e-f9ec6c7eab53)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/fe1db042-2401-4986-8fee-05f5964d98a0)

### ACCURACY
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/12ece598-71ac-4695-8070-ad9a0910c91b)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/db2b438d-1039-4e29-a1af-3f2537259147)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/c829077d-00ce-47e1-bfe8-e6b6b5b12c23)
 
### PREDICTION
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/f0c4efd2-f933-49b9-b477-4c74e30b8b31)
 
### CONFUSION MATRIX
 ![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/a1a36126-a6d4-4eb4-9561-ea5173e94e40)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/b2b4f8aa-1b74-4f5e-af82-327aef8e83c8)

### CLASSIFICATION REPORT
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/73f85d98-9271-4c18-b2d3-4d42df89f878)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/0b93000f-1266-4668-82aa-4ef16dbdec54)
 
### ROC AUC PLOT 
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/4bcfcd10-4f72-4677-ad07-16c5ce9eee44)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/1734bddb-ca43-4c0b-9ffd-3c3883554706)

### MODEL PREDICTION
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/2612e18f-6b1b-4310-a2a0-df3bc9f56c18)
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/68db821f-d026-40cd-b6d4-6f57a6af3a5c)
 
### PREDICT TEXT AND TOKENIZED
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/aa883286-b986-40a4-b2d3-c53d8cc08d46)

### PREDICTION OF THE MODEL
![image](https://github.com/Srividya-R123/Fake-News-Detection-using-NLP/assets/120908524/e97d94d8-d242-42ae-b4ed-7e1fb92f588e)

 


