# SMS Ham Spam Classification
SMS Spam collection is a dataset containing 5k+ SMS which can be mainly categorized into HAM and SPAM. The task is to build a Machine Learning models to predict the given SMS as HAM or SPAM.
![Alt text](https://lionbridge.ai/wp-content/uploads/2020/08/2020-08-20_nlp_spam-detection.jpg "SMS")
# Introduction
Short Message Service or SMS considered to be the text messaging service component of Telephone or Internet. In our day-to-day life we do receive considerable amount of SMS either from Friends, Telecom or Bank companies regarding our daily transactions or from tons of other sources. Some of these SMS texts are genuine whereas some can lead to fraudulent incidents. Main task of this case study is making a Machine Learning model which can predict the SMS as HAM or SPAM with the help of text body of SMS.
# Data
The dataset we used to build our model is from the UIC repostiory. The link to the dataset is here [link](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection). The dataset has 2 columns, the text messages and the label. The dataset contains 5572 text messages which are appropriately labelled ham and spam. The dataset is imbalanced in nature with 4825 instances of ham class and 747 instances of spam class. 

# Data Augumentation 
The SMS dataset is imbalanced dataset and this a problem where data belonging to one class (ham) is significantly higher than that belonging to other class(spam). Most ML/DL classification algorithms aren’t equipped to handle imbalanced classes and tend to get biased towards majority classes. There are multiple approaches to address data imbalance, here I will apply data augumentation to generate new spam SMS texts with the same meaning of the orignal spam texts that are already in the dataset.

# Approaches
In this work, comparative analysis will be conduct by applying two diffrent approches, one using TF-IDF with two traditional classifiers and another approache with fine-tune BERT for SMS classfication.

The required text preprocessing steps for TF-IDF are diffrenat than which are requierd using Bert for classification. TF-IDF is term frequency technique; Therefore, it need extra preproccessing steps.
### Fine_tuning Bert
- Preprocess text data for BERT and build PyTorch Dataset (tokenization, attention masks, and padding)
- Use Transfer Learning to build SMS Classifier using the Transformers library by Hugging Face
- Evaluate the model on test data
- Predict spam/ham on raw text


### Traditional Machine Learning Models 
- TF-IDF + SGD and Naive Bayes
# Execution 
The project has a jupyter notebook SMS_CLassification.ipynb which is used for the implementation of this project. Run each cell and you can observe the output of the commands.




# Conclusion
In the first approache I built a custom classifier using the Hugging Face library By adding a simple one-hidden-layer neural network classifier on top of BERT and fine-tuning BERT and trained it on SMS dataset. Both Naive Bayes and SGD classifier from simple Machine Learning model perform well. However, the performance evaluation on test set showed that fine-tuning Bert can achieve state-of-the-art performance. 
