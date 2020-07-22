---
layout: post
title:      "Quick and Easy GitHub Repo Setup and Sync with Local Folder"
date:       2020-07-22 00:14:51 +0000
permalink:  quick_and_easy_github_repo_setup_and_sync_with_local_folder
---


The simplest and most efficient way (for me anyways) to get a repo up and running on GitHub and in sync with your local project is laid out below.

First, of course, we need to set up a repo in GitHub. There are a few ways to do this, but the simplest way for me is to go to GitHub and:

1. On the GitHub Repositories page click on New
2. Type in the name of the new repo (username/project_name)
3. Click "Create Repository"

Now, on your computer:

1. Create a new directory (ex, mkdir new_proj or rails new new_proj)
2. Type **git init**
3. After writing a little code, type **git add .**
4. Type **git commit -m "first commit"** - you can call it whatever, but first commit is pretty common

Now that you have set the repo up locally and remotely it is now time to get them in sync:

1. In your terminal in your local directory, type git **remote add origin git@github.com:username/project_name**
2. Next, type **git push -u origin master**

That's it! Yous hould now be all set!

The next commit you will again lead with this flow: git add . > git commit > git push

Rinse and repeat. You are now up and running.

TIP: Commit often to ensure your code gets saved remotely


