# Milestone 3: Machine Learning

# Due date: December 5, 11:59pm

This milestone is worth 70 points. Thus, we expect you to put ***significant*** effort into this. 

**You should read through the entire milestone intructions before beginning your work! Don't start the cluster until you are ready.**

**Code and data saved locally on the cluster will be lost when the cluster terminates. Remember to save intermediate and analytical datasets in DBFS. Your deliverable artifacts (charts, summary csv files, etc.) must be saved in the `data/` folder of this repo.**

## Table of Contents


- [Milestone description](#milestone-description)
- [Analysis Requirements](#requirements-70-points)
- [Milestone web page requirements](#milestone-web-page-requirements)
- [Submission Instructions](#submission-instructions)

## Setup

1. Create a sub-directory named `ml` in the `code/` folder within the repository. Remember your cloned repo will be in the Databricks _Repos_ area. 
1. Create one or more Notebooks in the `ml` sub-directory as needed.

## Milestone description

In this milestone, you will develop Python and Pyspark notebooks to perform the following tasks: 

* Conduct machine learning on your big data
* Evaluate the performance of your models
* Interpret your results for your analytical questions
* Communicate your results on your group website

**REMEMBER!!! All the output you are making MUST be small data. Can you make a graph of all 1 million+ rows of spark data? NO! You MUST take that big data and collapse it into reasonable data to put into a table or a graph. You should never collect more than ~10,000 rows.**

## Requirements (70 points)

### Preparing data

-   Prepare your data for modeling. Conduct any remaining feature transformations and apply additional textual processing steps to have the needed variables in your data.

-   Conduct at 2 ML transformations for your data by applying string indexer, vectorizer, or other transformers.

-   Split data into testing and training data if you are running supervised models.

### Building machine learning models

-   Use machine learning to answer at least **two different business questions** (more is always fine!) from your data. Within each analysis, you will compare the performance of two or more models types by selecting at least two different hyperparameter sets OR at least two different pretrained models. The choice of hyperparameter/model comparison depends on your analysis.
  
- At least one of these model analyses must leverage Spark MLlib models where you conduct the training, testing, and validation yourself. The other analysis can pretrained models for your inference tasks.
  
### Evaluate model performance

-   Run model evaluation metrics (ROC AUC, Confusion Matrix, Accuracy, R2, etc.) on your models and/or hyperparameter options. 
  
- Evaluate your models using at least two different metrics and compare and interpret your results, for each ML analysis.
  
### Summarize your ML work

-   Prepare at least 1 appropriate table and at least 1 chart for each ML analysis. You do not need one for every model / hyperparameter set.

### Saving model output and using for inference

-   You must save at least one ML model into DBFS. Demonstrate that you can save your best ML model and load the prepared model into your notebook and start making predictions without any additional training. This can be done in a separate notebook.

### Pipeline bonus: **(+4 points)**: Apply pipelines to your ML analysis so that you can compare hyperparameters and model options without having to re-run large parts of code. Be sure to clearly indicate in your notebook and on your website the code you are implementing for the bonus.

## Milestone web page requirements

In this milestone, you will only be populating content in the ML page `website/ml.html` with the following sections:

### Executive summary

* Write 1-2 paragraphs on your ML accomplishments. You can include up to 2 images or tables. Your writing must be excellent and persuasive. 3 sentences total will not cut it. The expectation is to write at least 8 sentences. This is the section to describe the high-level results and the most important information only! This summary must be NON-TECHNICAL! Think about how to touch on your business goals without going into much detail.
  
### Analysis report

* Write a data analysis style report of 4-6 text paragraphs (each paragraph at least 4 sentences). This is where you will discuss your ML prep, execution, and evaluation. During that prose, you will present all your tables and figures. You can save the images or take snips from your Jupyter notebook. This part is for you to write up the analysis work you have already done. Be creative, be awesome!! Show off to a future employer your amazing data science skills!

    * The flow of the report is up to you. Maybe you want to split the text by business goal or organize the prose into a data journey story.
    * You must reference all the business goals that you have accomplished in this report. Did your technical proposal change as you started working with the data?
    * If you made changes to your business goals, discuss your analytical justification for changing your plans. It is OK that plans change, though it is important to describe why.
    * Your visualizations must follow the visualization best practices you learned in ANLY 503. There should be titles, axis labels, legends as needed, etc.

**Include links to all your NLP coding notebooks and sources for your external data so that your audience can look at your work. Make sure you put your exported notebooks into a public place so your audience can see your notebooks.**

## Submission instructions

1. Commit and push your files
1. Export any of the notebooks you created as IPython and/or html files, and add them to your repository from your local machine **before you tag the release** (these will not be committed from Databricks)
1. Tag the submission release commit with the `v0.3-ml` tag by the due date
1. Make sure to push to GitHub

