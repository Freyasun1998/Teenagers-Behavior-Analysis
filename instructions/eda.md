# Milestone 1: perform exploratory data analysis (EDA) and frame your analysis

**You can ignore these instructions since you have already done this.**

**You should thoroughly read through the entire assignment before beginning your work! Don't start the cluster until you are ready.**

**Code and data saved locally on the cluster will be lost when the cluster terminates. If you want to keep data, you must store it in DBFS. You must store the results (i.e. any plots, csv files) in the data folder of this repo.**

## First time setup

**NOTE**: only one cluster should be created per-group and be shared between all members of the group.

If this is your first time working on this repo, then you would need to perform the following steps. The details of how these steps are to be performed are available [ADB Setup guide](adb_setup.md).

If all of the following steps are successful then it means your environment is setup correctly and you are all set for begining your project.

1. Set up your git credentials.

1. Create a shared cluster for your team.

1. Clone this repo.

1. Create a notebook, call it `project_eda`.

1. In your new notebook, add the following code to an empty cell and confirm that you are able to see a list of files. If you get an error upon running this code then it means your cluster does not have access to the data, recheck your cluster creation steps.
    ```
    dbutils.fs.ls("abfss://anly502@marckvaismanblob.dfs.core.windows.net/reddit/parquet/comments")
    ```
1. Checkin the changed files (this would be the `project_eda` notebook) in the repo.

1. Export the `project_eda` notebook to `IPython Notebook` and checkin the `project_eda.ipynb` file in the repo.

## Submission Details (70 points)

In this assignment you will start working with your Reddit data, decide on the scope of your project, and outline your 10 business goals. 

You will use the file `project_starter_script.py` to get your reddit data from Azure Blob Storage, note that you do not need to copy the data to your local DBFS folder. The `project_starter_script.py` notebook also contains sample code for a basic EDA example and saving the results in the local repo so that it can be checked in. It also has an example to save intermediate big data to DataBricks File System (DBFS).

You will develop EDA notebook(s) using PySpark. All your big data analysis must be in PySpark. In this assignment you will examine the dataset, make transformations of the data, produce summary statistics and graphs of the data, and answer some of your business goals that only require exploratory work. You may choose to put all your work into one notebook or you may choose to separate it. Either is fine!

<p class="callout danger">
REMEMBER!!! All the output you are making MUST MUST MUST be small data. Can you make a graph of all 1 million+ rows of spark data? NO! You MUST MUST MUST take that big data and collapse it into reasonable data to put into a table or a graph. You should never collect more than ~10,000 rows back to you.
</p>

### Minimum requirements:

1. Make a project plan for your Reddit data with 10 topics that you plan on exploring.

   <b>Propose 10 different avenues of analysis for your data.</b>

    Any good data science project can be broken into at least 10 topics. These topics should vary in complexity to include exploratory, NLP, and ML ideas. Each entry of your 10 must include the "business goal" as well as the "technical proposal" for finding the answers. We want to see the "Executive Summary" view of the questions as well as the "Data Science" plans for making it happen.

    >Example question based on the data science subreddit https://www.reddit.com/r/datascience/Links to an external site.:

    >`Business goal`: Determine the most popular programming languages and the most effective programming languages used to conduct geospatial data analysis.  
    
    >`Technical proposal`: Use NLP to identify posts that mention geospatial terms and one or more programming languages. Conduct counts of which programming languages are mentioned the most along with these geospatial terms. Analyze counts over time to check for major deviations and identify the leaders. Conduct sentiment analysis of the posts to assign positive or negative values to programming languages. Present findings for volume metrics and sentiment analysis for the top 5 programming languages to answer the "popular" and "effective" insights for geospatial analysis.

    Each business goal must be 1-2 sentences while each technical proposal must be at least 3 sentences. There must be enough details about your plans so you can get feedback.<b> Include these business requirements in a markdown cell in the `project_eda` notebook.</b>

1. Conduct your exploratory data analysis.

-   Report on the basic info about your dataset. What are the interesting columns? What is the schema? How many rows do you have? etc. etc.

-   Conduct basic data quality checks! Make sure there are no missing values, check the length of the comments, remove rows of data that might be corrupted. Even if you think all your data is perfect, you still need to demonstrate that with your analysis.

-   Produce at least 5 interesting graphs about your dataset. Think about the dimensions that are interesting for your reddit data! There are millions of choices. Make sure your graphs are connected to your business questions.

-   Produce at least 3 interesting summary tables about your dataset. You can decide how to split up your data into categories, time slices, etc. There are infinite ways you can make summary statistics. Be unique, creative, and interesting!

-   Use data transformations to make AT LEAST 3 new variables that are relevant for your business questions. We cannot be more specific because this really depends on your project and what you want to explore!

-   Implement regex searches for specific keywords of interest to produce dummy variables and then make statistics that are related to your business questions. Note, you DO NOT have to do textual cleaning of the data at this point. The next assignment on NLP will focus on the textual cleaning and analysis aspect.

-   Find some type of external data to join onto your reddit data. Don't know what to pick? Consider a time-related dataset. Stock prices, game details over time, active users on a platform, sports scores, covid cases, etc., etc. While you may not need to join this external data with your entire dataset, you must have at least one analysis that connects to external data.

-   If you are planning to make any custom datsaets that are derived from your reddit data, make them now. These datasets might be graph focused, or maybe they are time series focused, it is completely up to you!

This assignment is worth 70 points. Thus, we expect you to put ***significant*** effort into this assignment. This assignment only requires the Jupyter notebooks.

### Extra Credit (10 points):

Create a website using your `project_eda` notebook. This could be as simple as publishing your notebook on GitHub pages.
- [Here](https://www.geeksforgeeks.org/publish-jupiter-notebook-file-as-web-app/) is a simple example that describes how to publish a notebook to GitHub.
- When you publish to GitHub, it will give you a warning that this repo is private but the published website would be Public, that is OK.

## Submitting the Assignment

You will follow the submission process for all labs and assignments:

1. Add all your requested files to the GitHub assignment repo for the appropriate deliverable.
1. Submit a final commit message called "final-submission" to your repo. This is critical so that instructional team can evaluate your work. Do not change your GitHub repo after submitting the "final-submission" commit message.

Make sure you commit **only the files requested**, and push your repository to GitHub!

The files to be committed and pushed to the repository for this assignment are:

-   `README.md`
-   `.gitignore`
-   `LICENSE`
-   `project_starter_script.py`
-   `project_eda.py`
-   `project_eda.ipynb` (export the Databricks notebook to generate this file)
-   `img/*`
-   `data/*`

<b>Make sure that your `project_eda` notebook includes both a list of the business problems you are solving and the charts and summary tables as described above in the minimum requirements section.</b>
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