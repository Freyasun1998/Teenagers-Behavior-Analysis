# Project NLP Assignment

## ANLY 502

**You should thoroughly read through the entire assignment before beginning your work! Don't start the cluster until you are ready.**

**Code and data saved locally on the cluster will be lost when the cluster terminates. If you want to keep data, you must store it in DBFS. You must store the results (i.e. any plots, csv files) in the data folder of this repo.**

## Cluster Setup

**NOTE**: only one cluster is allowed to be created per-group and be shared between all members of the group. If you want multiple clusters you would need to use smaller clusters.

1. Install the spark-nlp packages onto your cluster. You will have to restart the cluster.

Start by opening your cluster and going to the `Libraries` tab. Then click on the `Install New` button.

![](img/libraries-empty.png)

Add the `spark-nlp` python library from the PyPi repostitory. Use the version `4.2.1`. The entry to the Packges text box will be `spark-nlp==4.2.1`. Then click the blue `Install` button.

![](img/library-pypi.png)

Add the `spark-nlp` Java library from the Maven repostitory. Use the version `4.2.1`. The entry to the Coordinates text box will be `com.johnsnowlabs.nlp:spark-nlp_2.12:4.2.1`. Then click the blue `Install` button.

![](img/library-maven.png)

Now you should have installed both the packages you need to conduct your NLP work. Just import the library

![](img/libraries-confirmed.png)

1. Clone this repo.

1. Create a notebook, call it `project_nlp`.

1. In your new notebook, add the following code to an empty cell and confirm that you are able to see a list of files. If you get an error upon running this code then it means your cluster does not have access to the data, recheck your cluster creation steps.
    ```
    dbutils.fs.ls("abfss://anly502@marckvaismanblob.dfs.core.windows.net/reddit/parquet/comments")
    ```
1. Checkin the changed files (this would be the `project_nlp` notebook) in the repo.

1. Export the project_nlp notebook to IPython Notebook and checkin the project_nlp.ipynb file in the repo.

## Submission Details (70 points)

In this assignment you will conduct expand your analysis of Reddit data, merge your external data, and start to answer some of your analytical questions. 

You will use the file `project_starter_script.py` to get your reddit data from Azure Blob Storage, note that you do not need to copy the data to your local DBFS folder. The `project_starter_script.py` notebook also contains sample code for a basic EDA example and saving the results in the local repo so that it can be checked in. It also has an example to save intermediate big data to DataBricks File System (DBFS).

You will develop NLP notebook(s) using PySpark. All your big data analysis must be in PySpark. In this assignment you will examine the dataset, make transformations of the data, produce summary statistics and graphs of the data, and answer some of your business goals that only require exploratory work. You may choose to put all your work into one notebook or you may choose to separate it. Either is fine!

<p class="callout danger">
REMEMBER!!! All the output you are making MUST MUST MUST be small data. Can you make a graph of all 1 million+ rows of spark data? NO! You MUST MUST MUST take that big data and collapse it into reasonable data to put into a table or a graph. You should never collect more than ~10,000 rows back to you.
</p>

Minimum analytics requirements:

1. Conduct your natural language processing work.

-   Acquire, clean, and merge your external data source(s) onto your Reddit data. Produce appropriate charts/tables showing the distribution of your external data alongside your Reddit data.

-   Conduct basic data text checks / analysis on your data. What are the most common words overall or over time? What is the distribution of text lengths? What are important words according to TF-IDF?

-   Identify important keywords for your reddit data and use regex searches to create at least two dummy variables to identify comments of particular topics.

-   Clean your text data using johnsnowlabs sparkNLP. Think about a few standard procedures to use: stop words, stemming, lemmatizing, removing unusual characters, matching synonyms, etc. You must use at least five NLP cleaning procedures.

-   Build at least one sentiment model using the sparkNLP framework. Pick a pre-trained model or train your model! You can start off with simple pos/neg/neu sentiment. Maybe you will want to build your own textual classification model.... that is completely up to you and your topical interests and technical goals. You must report a table of summary statistics from any model(s) leveraged.

-   Produce at least 3 interesting graphs about your resulting dataset. Think about the dimensions that are interesting for your reddit data. There are millions of choices. Make sure your graphs are connected to your analytical questions.

-   Produce at least 3 interesting tables about your resulting dataset. You can decide how to split up your data into categories, time slices, etc. There are infinite ways you can make summary statistics. Be unique, creative, and interesting!

-   You must save your final dataset in parquet format into DBFS. This will allow you to more quickly work on your next assignment focused on ML without having to re-run any of your transformations.

2. Natural Language Processing Coding Notebooks

You will export your DataBricks notebooks to HTML so that you can include them directly in your project website. You will also export your DataBricks notebooks to .ipynb notebooks and upload them to your git repo. Make sure you follow good practice of providing markdown titles, subtitles, author information, section headers, comments in your code, etc.

#### **Website Construction**

In the prior milestone, you were offered extra credit to get your notebook up onto a website. **In this milestone and going forward, you will need to communicate the results of your analysis using a basic website.**

We **strongly recommend** building your website using GitHub Pages like you did in ANLY 503. This is the most straightforward and simple manner to build a site. You will have html outputs.

* Your interactive website **must be accessible via an `index.html` file in the site/ folder.** You can choose however you would like to build your website (using `Rmarkdown`, editing HTML directly, any other framework, etc.)

* Make sure that your code is well-organized and easy to read. Use separate files for your code notebooks and your main deliverable pages. Don't work with a messy repo and then try to clean it up before the final milestone. Comment your code early on!

The structure of the website will be as follows in the `website/` folder:
* Landing page - website/index.html (keep empty)
* Introduction page - website/introduction.html - (keep empty)
* EDA page - website/eda.html - (keep empty)
* NLP page - website/nlp.html - You are populating this site during milestone 2
* ML page  - website/ml.html - (keep empty)
* Conclusion page - website/conclusion.html - (keep empty)

In this milestone, you will only be populating content in the NLP page.

1. Natural Language Processing Page

You will create an NLP page for your group's project website. The format should be easy to access, but the method used could be Rmarkdown, HTML, etc. The communication needs to be effective with clean aesthetics, but you do not need to get too fancy. The page will contain the following:

* Part A: an executive summary consisting of 1-2 text paragraphs on your NLP accomplishments. You can include up to 2 images or tables. This is the section to describe the high-level results and the most important information only! This summary must be NON-TECHNICAL! Think about how to touch on your business goals without going into much detail.
    
* Part B: a data analysis style report of 4-6 text paragraphs (each paragraph at least 4 sentences). This is where you will discuss your NLP work and present all your interesting tables and figures. You can save the images or take snips from your DataBricks notebook. This part is for you to write up the analysis work you have already done. Be creative, be awesome!! Show off to a future employer your amazing data science skills!

    * The flow of the report is up to you. Maybe you want to split the text by business goal or organize the prose into a data journey story.
    * You must reference all the business goals that you have accomplished in this report. Did your technical proposal change as you started working with the data?
    * If you made changes to your business goals, discuss your analytical justification for changing your plans. It is OK that plans change, though it is important to describe why.
    * Your graphs must follow the visualization best practices you are learning in ANLY 503. There should be titles, axis labels, legends as needed, etc.

* Part C: Include links to all your NLP coding notebooks and sources for your external data so that your audience can look at your work. **Make sure you put your exported notebooks into a public place so your audience can see your notebooks.**

* Part D: Make sure your project website URL is at the top of your README.

This assignment is worth 70 points. Thus, we expect you to put ***significant*** effort into this assignment. This assignment only requires the Jupyter notebooks.

## Submitting the Assignment

You will follow the submission process for all labs and assignments:

1. Add all your requested files to the GitHub repo.
1. Make sure your project website URL is at the top of your README.
1. Tag a release of your project with tag version v0.2-nlp by the due date. Tagging a release allows you to continue the development, even before the mid-point is graded. [See instructions for creating releases on Github](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository) (This is in line with professional standards when using git). Your release must contain your first prototype implementation and a README.md with your writeup.

Push your code to GitHub.

Make sure you commit **only the files requested**, and push your repository to GitHub!

The files to be committed and pushed to the repository for this assignment are:

-   `README.md`
-   `.gitignore`
-   `LICENSE`
-   `project_starter_script.py`
-   `project_nlp.py`
-   `project_nlp.ipynb`
-   `img/*`
-   `data/*`
-   `website/*`

## Grading Rubric

Many of the assignments you will work on are open-ended. Grading is generally holistic, meaning that there will not always be specific point value for individual elements of a deliverable. Each deliverable submission is unique and will be compared to all other submissions.

- If a deliverable exceeds the requirements and expectations, that is considered A level work.
- If a deliverable just meets the requirements and expectations, that is considered A-/B+ level work.
- If a deliverable does not meet the requirements, that is considered B or lesser level work.

All deliverables must meet the following general requirements, in addition to the specific requirements of each deliverable:

If your the submission meets or exceeds the requirements, is creative, is well thought-out, has proper presentation and grammar, and is at the graduate student level, then the submission will get full credit. Otherwise, partial credit will be given and deductions may be made for any of the following reasons:

Points will be deducted for any of the following reasons:

- Any instruction is not followed
- There are missing sections of the deliverable
- The overall presentation and/or writing is sloppy
- There are no comments in your code
- There are files in the repository other than those requested
- There are absolute filename links in your code
- The repository structure is altered in any way
- Files are named incorrectly (wrong extensions, wrong case, etc.)