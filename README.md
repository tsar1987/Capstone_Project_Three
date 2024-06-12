# Binary Classification of Fake News and Real News
## Introduction
This project aims to develop a robust binary classification model to distinguish between fake news and real news articles.      
Using traditional machine learning method and NLP method and compare these two methods
## Audience
Journalists, editors, and media analysts who are interested in understanding and combating the spread of fake news.      
General Public: People interested in understanding how fake news is detected and differentiated from real news, as well as those concerned about the impact of misinformation on society.      
Researchers, scholars, and students interested in machine learning, natural language processing, or media studies.     
## Data
Train Dataset: 2 csv files from Kaggle      
fake news:   
23481 rows and 5 columns, including information about title, text, subject, date and label.
real news:   
21417 rows and 5 columns, including information about title, text, subject, date and label.
https://www.kaggle.com/datasets/bhavikjikadara/fake-news-detection      
Real_world unseen test set, 1 csv files      
Collect 25 pieces of news from internet.      
the 13 real news comes from reuters (7 news), cnn (2 news) and npr(4 news),      
the 12 real news comes from breitbart (5 news) and thegatewaypundit (7 news).   
## Exploratory Data Analysis
![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/a92be025-2c6d-440b-8190-b1139a028ec8)

Fake news 54.5%     Real news 45.5%    

![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/ef31b57e-823a-401d-8415-1241da4ad0a8)

News distribution by year is biased. 2015 and 2018 only fake news.        

![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/dae77a66-6505-4e32-84c4-d6866fd236c1)

Patterns of news distribution by months: more real news from Sept. to Dec.

![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/14187745-3796-4a0a-87bd-c8b2b3f484f9)

Patterns of news distribution by day: more fake news at weekends

![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/c640d5bd-820f-4ad8-bf7e-56fbfeb46930)

Distribution of news by day to election: more fake news before election

## Data Training and Modeling
Hyperparameter Table_Method_1    
![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/db20dbe0-643f-4ba6-bd6f-26e4506f636b)

Features Importance      
![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/c97e57ff-d6cb-4293-a7ea-43cf29242400)

Hyperparameter Table_Method_2       
![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/b2d451d4-078c-4cfd-aa32-3740ab67ef63)

Best Model Confusion Matrix on Test Set       
![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/ad7ef7f8-fcac-483b-8cdf-c1f92c49be1f)

High Coefficients Vectors for Real News Classification    
![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/16128ab1-f6aa-4cd0-b0ae-7d8c030e9922)

High Coefficients Vectors for Fake News Classification
![image](https://github.com/tsar1987/Capstone_Project_Three/assets/125304961/39cd6e75-2156-4400-91d2-4a47f1d212e6)

## Conclusion
Two modeling methods were used for this project. Method_2 performs better than Method_1 overall, which makes sense, means natural language processing method can be generalized better.    
It is very difficult to decide better one from CountVectorizer and TfidfVectorizer.      
The top 6 vectors for determining real news are: Wednesday, Thursday, Tuesday, Friday, Monday, said.         
The top 6 vectors for determining fake news are: just, this, these, even, Hillary, us.       
Using CountVectorizer and TfidfVectorizer with different parameters didn’t change these high coefficient vectors much.        

## Future Work
Try other vectorize methods using packages like spacy, genism, sentence_transformer etc.    
spacy vector, word2vec, doc2vec and sentence_transformer.        
All these four methods work differently as CountVectorizer and TfidfVectorizer. In CountVectorizer and TfidfVectorizer, each vector corresponds to a unique word in the vocabulary. Therefore, interpreting the logistic regression coefficients is straightforward. However, with spacy, word2vec, doc2vec and BERT embeddings, each vector captures complex relationships and context-dependent information from the text. Interpreting the coefficients becomes more challenging because each dimension does not  directly correspond to a word.          

 






























