# Stackoverflow-Tag-prediction

### Data source -https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/

### Description
- Stack Overflow is the largest, most trusted online community for developers to learn, share their programming knowledge, and build their careers.
- Stack Overflow is something which every programmer use one way or another. Each month, over 50 million developers come to Stack Overflow to learn, share their knowledge, and build their careers. It features questions and answers on a wide range of topics in computer programming. The website serves as a platform for users to ask and answer questions, and, through membership and active participation, to vote questions and answers up or down and edit questions and answers in a fashion similar to a wiki or Digg. As of April 2014 Stack Overflow has over 4,000,000 registered users, and it exceeded 10,000,000 questions in late August 2015. Based on the type of tags assigned to questions, the top eight most discussed topics on the site are: Java, JavaScript, C#, PHP, Android, jQuery, Python and HTML

**Problem Statement**
- Suggest the tags based on the content that was there in the question posted on Stackoverflow.

**Business Objective and cosntraints**
- Predict as many tags as possible with high precision and recall.
- Incorrect tags could impact customer experience on StackOverflow.
- No strict latency constraints.

**Data Overview**
- All of the data is in 2 files: Train and Test.
- **Train.csv** contains 4 columns: Id,Title,Body,Tags.
- **Test.csv** contains the same columns but without the Tags, which you are to predict.
- Size of Train.csv- 6.75GB
- Size of Test.csv- 2GB
- Number of rows in Train.csv = 6034195

The questions are randomized and contains a mix of verbose text sites as well as sites related to math and programming. The number of questions from each site may vary, and no filtering has been performed on the questions (such as closed questions).

Data field explanation
- Dataset contains 6,034,195 rows. The columns in the table are
- **Id** - Unique identifier for each question
- **Title** - The question's title
- **Body** - The body of the question
- **Tags** - The tags associated with the question in a space-seperated format (all lowercase, should not contain tabs '\t' or ampersands '&')

**Machine learning problem**
- It is a multi-label classification problem
- Multi-label Classification</b>: Multilabel classification assigns to each sample a set of target labels. This can be thought as predicting properties of a data-point that are not mutually exclusive, such as topics that are relevant for a document. A question on Stackoverflow might be about any of C, Pointers, FileIO and/or memory-management at the same time or none of these.
- __Credit__: http://scikit-learn.org/stable/modules/multiclass.html

**Performance metric**
- Micro avergaed F1 score(Mean F1 score) 
- micro f1 score
- Macro F1 score
- Hamming Loss

