# Milestone 2: add external data and run NLP

This milestone is worth 70 points. Thus, we expect you to put ***significant*** effort into this. 

**You should read through the entire milestone intructions before beginning your work! Don't start the cluster until you are ready.**

**Code and data saved locally on the cluster will be lost when the cluster terminates. Remember to save intermediate and analytical datasets in DBFS. Your deliverable artifacts (charts, summary csv files, etc.) must be saved in the `data/` folder of this repo.**

## Table of Contents

- [Setup for NLP](#setup)
- [Milestone description](#milestone-description)
- [Analysis Requirements](#requirements-70-points)
- [Milestone web page requirements](#website-setup)
- [Submission Instructions](#submitting-the-assignment)

## Setup

1. [Follow these instructions](sparknlp.md) to install the SparkNLP package on your cluster. You only need to do this once for a given cluster.
1. Create a sub-directory named `nlp` in the `code/` folder within the repository. Remember your cloned repo will be in the Databricks _Repos_ area. 
1. Create one or more Notebooks in the `nlp` sub-directory as needed.

## Milestone description

In this milestone, you will develop Python and Pyspark notebooks to perform the following tasks: 

* Expand your analysis of Reddit data
* Conduct NLP processing work
* Merge/overlay your external data, including EDA
* Start to answer some of your analytical questions.

**REMEMBER!!! All the output you are making MUST be small data. Can you make a graph of all 1 million+ rows of spark data? NO! You MUST take that big data and collapse it into reasonable data to put into a table or a graph. You should never collect more than ~10,000 rows.**

## Requirements (70 points)

### Add external data

-   Acquire, clean, and merge your external data source(s) onto your Reddit data. Produce appropriate charts/tables showing the distribution of your external data alongside your Reddit data.

### Conduct your natural language processing work.

-   Conduct basic data text checks / analysis on your data. What are the most common words overall or over time? What is the distribution of text lengths? What are important words according to TF-IDF?

-   Identify important keywords for your reddit data and use regex searches to create at least two dummy variables to identify comments of particular topics.

-   Clean your text data using johnsnowlabs sparkNLP. Think about a few standard procedures to use: stop words, stemming, lemmatizing, removing unusual characters, matching synonyms, etc. You must use at least five NLP cleaning procedures.

### Build a sentiment model

-   Build at least one sentiment model using the sparkNLP framework. Pick a pre-trained model or train your model! You can start off with simple pos/neg/neu sentiment. Maybe you will want to build your own textual classification model.... that is completely up to you and your topical interests and technical goals. You must report a table of summary statistics from any model(s) leveraged.

### Visualize

-   Produce at least 3 interesting graphs about your resulting dataset. Think about the dimensions that are interesting for your reddit data. There are millions of choices. Make sure your graphs are connected to your analytical questions.

### Summary tables

-   Produce at least 3 interesting tables about your resulting dataset. You can decide how to split up your data into categories, time slices, etc. There are infinite ways you can make summary statistics. Be unique, creative, and interesting!

### Save output

-   Save your output datasests in parquet format into DBFS. This will allow you to more quickly work on your next assignment focused on ML without having to re-run any of your transformations.

## Milestone web page requirements

In this milestone, you will only be populating content in the NLP page `website/nlp.html` with the following sections:

### Executive summary

* Write 1-2 paragraphs on your NLP accomplishments. You can include up to 2 images or tables. This is the section to describe the high-level results and the most important information only! This summary must be NON-TECHNICAL! Think about how to touch on your business goals without going into much detail.
    
### Analysis report

* Write a data analysis style report of 4-6 text paragraphs (each paragraph at least 4 sentences). This is where you will discuss your NLP work and present all your interesting tables and figures. You can save the images or take snips from your Databricks notebook. This part is for you to write up the analysis work you have already done. Be creative, be awesome!! Show off to a future employer your amazing data science skills!

    * The flow of the report is up to you. Maybe you want to split the text by business goal or organize the prose into a data journey story.
    * You must reference all the business goals that you have accomplished in this report. Did your technical proposal change as you started working with the data?
    * If you made changes to your business goals, discuss your analytical justification for changing your plans. It is OK that plans change, though it is important to describe why.
    * Your visualizations must follow the visualization best practices you learned in ANLY 503. There should be titles, axis labels, legends as needed, etc.

**Include links to all your NLP coding notebooks and sources for your external data so that your audience can look at your work. Make sure you put your exported notebooks into a public place so your audience can see your notebooks.**

## Submission intructions

1. Commit and push your files
1. Export any of the notebooks you created as IPython and/or html files, and add them to your repository from your local machine **before you tag the release** (these will not be committed from Databricks)
1. Tag the submission release commit with the `v0.2-nlp` tag by the due date
1. Make sure to push to GitHub


