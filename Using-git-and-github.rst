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
    #. Add your github repository as a remote to your local repository
#. Contribute to someone else's codebase
    #. Fork a project
    #. Create a new fix or feature
    #. Submit a pull request
    #. Merge a pull request (as an owner)
#. Concepts to remember
    #. Forking
    #. Cloning
    #. Fetching
    #. Pulling
    #. Pushing


Quick Legend
------------

::

    $ monospace text starting with a dollar sign means type this command verbatim
    ...except for anything in <angle brackets>, which means 'fill in the name of something' as applies


Get and use git locally
=======================

Install git
-----------

Go to ``http://git-scm.com``

Hit Downloads

Highly recommend installing Git BASH in Windows


Prepare your codebase
---------------------

Make a Code directory in your Documents

.. code-block:: bash

    $ mkdir Code
    $ cd Code

Put your initial files into the new directory
        

Run git
-------

Run Git BASH in Windows, or open a terminal in Linux/OS X

Move to your code directory

.. code-block:: bash

    $ cd Code

Configure your username and email with git

.. code-block:: bash

    $ git config --global user.name "<your name>"
    $ git config --global user.email "<your email address"


Create a repository
-------------------

Create a new project directory

.. code-block:: bash

    $ mkdir <project directory>
    $ cd <project directory>

Initialize a repository

.. code-block:: bash

    $ git init .

Check that your repository is set up

.. code-block:: bash

    $ git status


Track your work
---------------

Make your changes

    Create a new file, or modify an existing one

Add each changed file to the commit

.. code-block:: bash

    $ git add <filename>

Create the new commit

.. code-block:: bash

    $ git commit -m "<Short descriptive title>"


Organize your changes
---------------------

Create a new feature branch

.. code-block:: bash

    $ git checkout -b <new-feature>

Make your changes

    Create a new file, or modify an existing one

Add each changed file to the commit

.. code-block:: bash

    $ git add <filename>

Create the new commit

.. code-block:: bash

    $ git commit -m "<Short descriptive title>"

Add more files and commits as needed

Check out your master branch when you're done with the feature

.. code-block:: bash

    $ git checkout master

Merge your feature branch onto master

.. code-block:: bash

    $ git merge <new-feature>

Delete the now-merged branch

.. code-block:: bash

    $ git branch -d <new-feature>


Use git with github
===================

Get started with github
-----------------------

Go to ``http://github.com``

Create an account

Log in and look around


Create a repository on github
-----------------------------
 
Click the big plus sign in the top right corner

Click New repository

Name your repository

    *Try to avoid characters outside of a-zA-Z0-9 and _*

Give it a short description

    *You can change this later.*

Keep it public for now

Don't "Initialize this repository with a README"

Don't "Add .gitignore" or "Add a license"

    *You can change these later.*

Hit the big green button


Add your github repository as a remote to your local repository
---------------------------------------------------------------

Copy that HTTPS URI from the github repository Quick Setup instructions

    ``https://github.com/<your account name>/<your repository name>.git``

Back to your repository locally

Check your repository's remotes

.. code-block:: bash

    $ git remote -v

Add your github remote to your local repository and call it ``origin``

.. code-block:: bash

    $ git remote add origin <that url you just copied>

Refresh your local copy of each of your remotes

.. code-block:: bash

    $ git fetch --all

Check your remotes list again

.. code-block:: bash

    $ git remote -v

*Notice you've got two targets, one for fetch and one for push.*

Overwrite your github repository's master branch with your local repository's version

.. code-block:: bash

    $git push origin master
    Username: <your github username>
    Password: <your password>

*Your password won't show as you type it.*

Refresh your repository page on github to see the changes.


Contribute to someone else's codebase
=====================================

Fork a project
--------------

Find someone else's project on github

Click the Fork button in the top right corner

Copy the HTTPS clone URL from your fork's page, bottom right

Clone your fork locally 

.. code-block:: bash

    $ git clone <your fork's URI> <new project directory>

Go into the new project directory

.. code-block:: bash

    $ cd <new project directory>

Check out your remotes

.. code-block:: bash

    $ git remote -v

*Notice you already have an* ``origin`` *remote.*

Go back to your friend's repo

Copy their HTTPs clone URL from the bottom right

Add your friend's repo as the remote ``upstream``

.. code-block:: bash

    $ git remote add upstream <your friend's URI>``

Fetch all of your friend's changes and branches

.. code-block:: bash

    $ git fetch --all


Create a new fix or feature
---------------------------

Make sure your codebase is up to date

.. code-block:: bash

    $ git checkout master
    $ git fetch --all
    $ git pull upstream master

Create a new feature branch

.. code-block:: bash

    $ git checkout -b <new-feature>

Make your changes and commits

Push your branch to **your** remote

.. code-block:: bash

    $ git push origin <new-feature>


Submit a pull request
---------------------

Go to **your** fork of the project on github

Find the feature branch

Click "Create Pull Request"


Merge a pull request (as an owner)
----------------------------------

Go to **your** project on github

Click on "Pull requests" on the right

Click the title of a request

Review the changes, add comments as necessary

Click "Merge" if you like it

Optionally click "Delete Branch"


Concepts to remember
====================

Forking (for our purposes) copies a repository on github to another repository on github

Cloning (for our purposes) copies a repository on github to your local machine

Fetching gets updates from remotes and stores them on your local machine

Pulling only gets updates from local copies of remotes

    *You have to fetch first if you want someone else's updates.*

Pushing sends changes from a local branch to a branch of a remote
