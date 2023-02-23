# Milestone 4: Final Deliverable (90 points)

This finale milestone is worth 90 points. Thus, we expect you to put ***significant*** effort into this. 

**You should read through the entire milestone intructions before beginning your work! Don't start the cluster until you are ready.**

**Code and data saved locally on the cluster will be lost when the cluster terminates. Remember to save intermediate and analytical datasets in DBFS. Your deliverable artifacts (charts, summary csv files, etc.) must be saved in the `data/` folder of this repo.**

## Table of Contents

- [Milestone description](#milestone-description)
- [Analysis Requirements](#analysis-requirements)
- [Milestone web page requirements](#final-milestone-web-page-requirements)
- [Submission Instructions](#submission-instructions)

## Setup

Since you are making updates to your code you do not need to make any new subdirectories. Be sure to indicate on your website or in your Git repo which parts of your project have been updated.

## Milestone description

In this assignment you will complete your project, making sure that it is **ready for primetime**. This means that your project website has been improved since your intermediate assignments and will wow any future employers.

You will populate the following pages:
- `website/index.html`
- `website/eda.html`
- `website/conclusion.html`

You will udpate and improve the following pages:
- `website/nlp.html`
- `website/ml.html`

Remember, all your big data analysis must be in PySpark unless an exception has been made. You may choose to put all your work into one notebook or you may choose to keep separate notebooks for your work. It might be the case that you have to do very little additional coding for your final deliverable. This really depends on the status of your existing project work and how much more effort you have to put into building it out to be great! More refinement is always better! Iteration always helps! Keep improving the project!

## Analysis Requirements

-   Expand on your analysis from the intermediate assignments in some manner. Do you add an additional data transformation? Try one more model? Try a different NLP text method? It does not have to be groundbreaking at this point, but think about how you can make minor updates to improve the work further.
-   Make sure to indicate in an appendix on your conclusion page what updates you made to your analysis since your intermediate deliverables.

## Final milestone web page requirements

### Reviewing and editing your existing website

-   Spell check, grammar check, read for clarity. Make sure all your pages are well-written and free of errors!

-   Submit all your notebooks used in the project to the Git repo. You must also have all your notebooks available on your website. Make sure you have these notebooks available in html format that is easily viewable as a web user. Points will be deducted for linking to ipynb files that must be downloaded.

-   Can your audience access all of your code files?

-   Just the ipynb is not a valid webpage. It is really hard to navigate. You need to save your outputs and create the webpages, suitable for a non-data scientist audience.

-   A public website is encouraged but absence of a public website will not be penalized. However, your team MUST have a self-contained website that can be opened locally upon download. You can assume an available internet connection (in case you are calling JS libraries.

-   If you do choose to publish your website publicly, you must update the README to include its URL.

### Introduction page

-   You will write up an introduction for your entire project of at least 4 text paragraphs and 2-5 informative graphs/images/tables.

-   This is a NON-TECHNICAL introduction. There should be no technical language, equations, etc. Talk about what the project, its goals, and why it matters!

-   All your analytical goals/questions and technical proposals must be listed out at the end as an appendix to your introduction.

-   Adapt your project plan analytical goals/questions with any changes you have made to your project since you started.

-   It is OK if you did not get to all of your analytical goals/questions.

### NLP and ML pages

-   You made these pages in earlier deliverables. This means you only have to make updates and improvements to these two pages.

-   Improve usability of your pages by fixing issues with html, placement, blurry graphics, etc.

-   **Strengthen the analytical justification of the decisions you made in your project.** This text is critical so the audience understands why you followed the path of work that you did.

### Conclusion page

-   You will write up 3-5 text paragraphs with 2-5 informative graphs/images/tables that summarize and conclude on all the existing work you have done in the project,

-   You must have a section that discusses planned next steps in the project. It does not mean that you will actually implement these next steps, but it is important to outline your vision for how you would move the project forward if you had another month to conduct your work.

-   Make sure you are **not** repeating yourself from the methods pages.

-   The introduction and conclusion should serve as book ends to your project. If those pages are read without any of the middle pages, one should still be able to understand the purpose of the project, its impact, and your next steps.
    
### EDA page

Your `website/eda.html` will be populated with the following sections:

#### Executive summary

* Write 1-2 paragraphs on your EDA accomplishments. You can include up to 2 images or tables. Your writing must be excellent and persuasive. 3 sentences total will not cut it. The expectation is to write at least 8 sentences. This is the section to describe the high-level results and the most important information only! This summary must be NON-TECHNICAL! Think about how to touch on your business goals without going into much detail.
    
#### Analysis report

* Write a data analysis style report of 4-6 text paragraphs (each paragraph at least 4 sentences). This is where you will discuss your data ingestion, data cleaning, and data evaluation. During that prose, you will present all your tables and figures. You can save the images or take snips from your Jupyter notebook. This part is for you to write up the analysis work you have already done. Be creative, be awesome!! Show off to a future employer your amazing data science skills!

    * The flow of the report is up to you. Maybe you want to split the text by business goal or organize the prose into a data journey story.
    * You must reference all the business goals that you have accomplished in this report. Did your technical proposal change as you started working with the data?
    * If you made changes to your business goals, discuss your analytical justification for changing your plans. It is OK that plans change, though it is important to describe why.
    * Your visualizations must follow the visualization best practices you learned in ANLY 503. There should be titles, axis labels, legends as needed, etc.

**Include links to all your EDA coding notebooks and sources for your external data so that your audience can look at your work.**

- ipynb files MUST show the requisite outputs, they will be penalized even if the code is present. We need to see the outputs from your coding cells in addition to your website.

## Submission instructions

1. Commit and push your files
1. Export any of the notebooks you created as IPython and/or html files, and add them to your repository from your local machine **before you tag the release** (these will not be committed from Databricks)
1. Tag the submission release commit with the `v1.0-final` tag by the due date
1. Make sure to push to GitHub


