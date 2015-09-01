===============
Github Workshop 
===============

-----------
Ed Cranford
-----------
 
Table of Contents
=================
 
    #. Get and use git locally
        #. Install git
        #. Prepare your codebase
        #. Run git
        #. Create a repository
        #. Track your work
        #. Organize your changes
    #. Use git with github
        #. Get started with github
        #. Create a repository on github
        #. Add the github repository as a remote to your local repository
    #. Contribute to someone else's codebase
        #. Fork a project
        #. Create a new fix or feature
        #. Submit a pull request
        #. Merge a pull request (as an owner)
    #. Concepts to remember


Quick Legend
------------
    - ``$ monospace text starting with a dollar sign means type this command verbatim,``
    - ``except for anything in <angle brackets>, which means 'fill in the name of something' as applies``
    - **Bold steps mean they're new since the last section**


Get and use git locally
=======================

Install git
-----------

    - Go to ``http://git-scm.com``
    - Hit Downloads
    - Highly recommend installing Git BASH in Windows


Prepare your codebase
---------------------

    - Make a Code directory in your Documents
        - ``$ mkdir Code``
        - ``$ cd Code``
    - Put your initial files into the new directory
        

Run git
-------

    - Run Git BASH in Windows, or open a terminal in Linux/OS X
    - Move to your code directory
        - ``$ cd Code``
    - Configure your username and email with git
        - ``$ git config --global user.name "<your name>"``
        - ``$ git config --global user.email "<your email address"``
 

Create a repository
-------------------

    - Create a new project directory
        - ``$ mkdir <project directory>``
        - ``$ cd <project directory>``
    - Initialize a repository
        - ``$ git init .``
    - Check that your repository is set up
        - ``$ git status``


Track your work
---------------

    - Make your changes
        - Create a new file or modify an existing one
    - Add each changed file to the commit
        - ``$ git add <filename>``
    - Create the new commit
        - ``$ git commit -m "<Short descriptive title>"``


Organize your changes
---------------------

    - **Create a new feature branch**
        - ``$ git checkout -b <new-feature>``
    - Make your changes
        - Create a new file or modify an existing one
    - Add each changed file to the commit
        - ``$ git add <filename>``
    - Create the new commit
        - ``$ git commit -m "<Short descriptive title>"``
    - Add more files and commits as needed
    - **Check out your master branch when you're done with the feature**
        - ``$ git checkout master``
    - **Merge your feature branch onto master**
        - ``$ git merge <new-feature>``
    - **Delete the now-merged branch**
        - ``$ git branch -d <new-feature>``


Use git with github
===================

Get started with github
-----------------------

    - Go to ``http://github.com``
    - Create an account
    - Log in and look around

Create a repository on github
-----------------------------
 
    - Click the big plus sign in the top right corner
    - Click New repository
    - Name your repository
        - Try to avoid characters outsides of a-zA-Z0-9 and _
    - Give it a short description
        - You can change this later
    - Keep it public for now
    - Don't "Initialize this repository with a README"
    - Don't "Add .gitignore" or "Add a license"
        - You can change these later
    - Hit the big green button


Add the github repository as a remote to your local repository
--------------------------------------------------------------

    - Copy that HTTPS URI from the github repository Quick Setup instructions
        - ``https://github.com/<your account name>/<your repository name>.git``
    - Back to your repository locally
    - Check your repository's remotes
        - ``$ git remote -v``
    - Add your github remote to your local repository and call it ``origin``
        - ``$ git remote add origin <that url you just copied>``
    - Refresh your local copy of each of your remotes
        - ``$ git fetch --all``
    - Check your remotes list again
        - ``$ git remote -v``
    - Overwrite your github repository's master branch with your local repository's version
        - ``$git push origin master``
        - ``Username: <your github username>``
        - ``Password: <your password>``
            - Your password won't show as you type it.
    - Refresh your repository page on github and you'll see the changes.


Contribute to someone else's codebase
=====================================

Fork a project
--------------

    - Find someone else's project on github
    - Click the Fork button in the top right corner
    - Copy the HTTPS clone URL from your fork's page, bottom right
    - ``$ git clone <your fork's URI> <new project directory>``
    - ``$ cd <new project directory>``
    - ``$ git remote -v``
        - notice your already have an ``origin`` remote
    - Go back to your friend's repo
    - Copy their HTTPs clone URL from the bottom right
    - ``$ git remote add upstream <your friend's URI>``
    - ``$ git fetch --all``


Create a new fix or feature
---------------------------

    - Make sure your codebase is up to date
        - ``$ git checkout master``
        - ``$ git fetch --all``
        - ``$ git pull upstream master``
    - Create a new feature branch
        - ``$ git checkout -b <new-feature>``
    - Make your changes and commits
    - Push your branch to **your** remote
        - ``$ git push origin <new-feature>``


Submit a pull request
---------------------

    - Go to **your** fork of the project
    - Find the feature branch
    - Click "Create Pull Request"


Merge a pull request (as an owner)
----------------------------------

    - Go to **your** project
    - Click on "Pull requests" on the right
    - Click the title of a request
    - Review the changes, add comments as necessary
    - Click "Merge" if you like it
    - Optionally click "Delete Branch"


Concepts to remember
====================

    - Forking (for our purposes) copies a repository on github to another repository on github
    - Cloning (for our purposes) copies a repository on github to your local machine
    - Fetching gets updates from remotes and stores them on your local machine
    - Pulling only gets updates from local copies of remotes
        - You have to fetch first if you want someone else's updates
    - Pushing sends changes from a local branch to a branch of a remote
