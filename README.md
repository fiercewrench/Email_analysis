# Email Analysis, LDA, TextRank

## Overview

### Email Analysis
• Detected the spam emails and classify the non-spam emails into groups according to importance

• Extracted emails from Outlook application and conduct data preprocessing, including converting the datasets to dataframe, removing HTML markup, dividing the data into the training set and testing set

• Implemented the TF-IDF algorithm to represent an email using a vector according to the term frequency

• Built two models for detecting spam email using Naïve Bayes Classifier and SVM Classifier respectively and found that SVM Classifier achieve higher accuracy score

### LDA
• Implemented the bag-of-words model to represent an email using a vector

• Applied LDA (Latent Dirichlet Allocation) model to the non-spam emails and generate 10 topic clusters (the number of keywords in each clusters can be changed at anytime)

### TextRank
• Use textRank to find the top n frequent words in the doc compared with IF-IDF algorithm

  (Each word is a node and any two-word pairs in a window are considered have an undirected edge. Based on the graph, we can calculated the weight for each node (word). The most important words will be extracted and used as keywords.)


	
## Used Packages

词形还原工具 (将不同词性的词都还原成原始词性)
from nltk.stem.wordnet import WordNetLemmatizer
lemma = WordNetLemmatizer()

词袋模型
from sklearn.feature_extraction.text import CountVectorizer

去除html tag
from bs4 import BeautifulSoup

"结巴"中文分词
(有写这个package的code，但实际上并没有真正用到，因为email都是英文的）
import jieba.posseg as pseg
https://pypi.org/project/jieba/

managing email messages
import email

lda package
import lda
lda.lda


	
