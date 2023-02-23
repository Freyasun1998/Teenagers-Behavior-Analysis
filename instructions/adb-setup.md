# Azure DataBricks Setup

This document lists the steps for the various tasks needed to get Azure DataBricks up and running in your Azure account.


## Login to the ADB Workspace for the first time through the portal to be added to the workgroup

1. Login to portal.azure.com with GU credentials

1. Go to Subscriptions
1. Find the `ANLY502-Fall2022-Project` subscription. If not shown, click on the _subscriptions_ bubble and uncheck the _show only the subscriptions selected in the global subscription filter_
1. Click on the subscription
1. From the subscription summary page, clock on `Resource Groups`
1. Find the resource group with the same name as your project grop i.e. `project-group-xx` (**not** the ones beginning with `databricks`)
1. Click on the RG
1. Click on the Databricks resource named `project-group-xx-workspace`
1. Click on Launch Workspace
1. Bookmark the workspace URL to be able to navigate to it directly in the future
1. The user will be added to the workspace. All TA's and instructors have access to all workspaces, but students are limited to only their particular one

## Enable DBFS Browsing within the ADB Workspace

1. click on your email address on the top right
1. Click on Admin Console
1. Go to the WOrkspace settings tab
1. Scroll down an turn on _DBFS File Browser_
1. Refresh browser

## Create a shared folder for the project

1. On the left nav bar Select Workspace > Shared > Create > Folder
1. In the project folder import the starter `.dbc` with the credentials to read data


## Create a cluster
1. Click on Compute on the left nav bar
1. Click on Create Cluster. Makre sure to select DataBricks Runtime version as 11.3 or higher.
1. Name the cluster "Project Team Cluster"
1. Select _Unrestricted_ as the Policy
1. Select Multi-node
1. Select _No isolation shared_ in the Access Mode dropdown
1. Change the Terminate after value from 120 to 60
1. Expand the `Advanced options` section and in the text area for `Spark Config` copy paste the credentials information provided to you via Canvas. **Note that this step is required to access the raw data that you need for your project. Your cluster will not be able to access the data without these credentials. Make sure you copy paste as-is from the Canvas announcement.`**
1. Click on _Create Cluster_

## Setup Git Credentials

1. Click on your username on the top-right hand corner of the screen and then click on `User Settings` from the drop down menu.
![](img/adb-user-settings.png)
1. Click on the `Git Integration` tab.
![](img/adb-user-settings-git.png)
1.Select `Git provider` as `GitHub` from the dropdown and enter your GitHub username and Personal Access Token (you should have this from lab 1).
![](img/adb-user-settings-git-creds.png)
1. Click the `Save` button to save the Git integration settings.
![](img/adb-user-settings-git-creds-save.png)


## Working with Git Repos

### Add A Repo

1. Click on the `Repos` menu item on the sidebar.
![](img/adb-repos.png)

1. Click on the `Add Repo` button. Enter the Git URL for the repo to be cloned. Note that this would be the `https` URL for the repo (uptil now we have been cloning repos using `git` with the SSH key, now we will be cloning repos via the `https` URL using the `personal access token`). The repo URL in the screenshot below is simply an example, your repo URL would be your GitHub classroom URL.
![](img/adb-repos-add-repo.png)

1. Once the repo gets cloned, it will appear in the repo list.
![](img/adb-repos-cloned-repo.png)

### `Pull` latest changes from Git

1. Right click on the Repo name in the Repos list to reveal the Git menu.
![](img/adb-repos-git-menu.png)

1. Clck on `Git` menu item. A popup dialogbox would come up, click on the `Pull` button from the top-right corner.
![](img/adb-repos-git-pull.png)

1. Another popup dialog box would come up, click on the `Confirm` button (You should not have any uncommited changes at this point that could be overwritten by the git pull).
![](img/adb-repos-git-pull-popup.png)

1. Once the pull completes, new and/or updated files will show up in the cloned repo.

### `Commit` & `Push` latest changes to Git

1. 1. Right click on the Repo name in the Repos list to reveal the Git menu.
![](img/adb-repos-git-menu.png)

1. Clck on `Git` menu item. Now you should see any new/changed files in the changes list. Add a descriptive comment and click the `Commit & Push` button.
![](img/adb-repos-git-commit-and-push.png)

1. Once the commit and push is successful you should see a notification on the top-right corner of your browser window.
![](img/adb-repos-git-commit-and-push-successful.png)

## Create a new Notebook

1. Right click on the menu that is showing the files in a repo and click on `Create` -> `Notebook`.
![](img/adb-create-notebook.png)

1. A dialog box will popup for new notebook creation, provide a appropriate name for the notebook. Select a cluster for the nhotebook (this would be your group's shared project cluster). Click on the `Create` button.
![](img/adb-create-notebook-2.png)

1. A new notebook will be created.
![](img/adb-create-notebook-3.png)

1. Checkin this new notebook into the repository.
