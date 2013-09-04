Author
==========
"Kosir, Jonathan", kosirjm
01_Git_and_Intro
================

Practice with basic git functions, and intro to study of Data Structures

Reading
=======

**Version Control with Git, 2nd Ed**. Loeliger and McCullough. 

http://proquest.safaribooksonline.com/book/databases/content-management-systems/9781449345037/version-control-with-git/id302681?uicode=ohlink (Free access through www.lib.miamioh.edu, but limited to 100 simultaneous users across all OhioLink. I recommend downloading/printing the required readings ahead of time, just in case.)

Read only the following:

1. Chapter 1
  * Background
  * The Birth of Git
2. Chapter 3: Getting Started
  * Intro
  * The Git Command Line
  * Quick Introduction to Using Git (read all sections)
  * Configuration files (Intro only, may skip part on aliases)
3. Chapter 4: Basic Git Concepts
  * Basic concepts (read all)
  * Object store pictures
  * Git concepts at work (read all)
4. Chapter 21: Git and Github

**Open Data Structures in C++**. Morin. 

http://opendatastructures.org/ (Free access. I recommend downloading the PDF version.)

Read the following:

1. Chapter 1 (pp. 1-20)

Homework
========

1. Create an account with github.com. You may select the free account. If you want to get some free private repos, you may apply at https://github.com/edu
2. Go to https://github.com/MiamiOH-CSE274/01_Git_and_Intro and fork the repo, which will create a copy of it in your github account.
3. Install git on your computer, if you do not already have it. I recommend installing http://windows.github.com/ if you use windows, or http://mac.github.com/ if you use Mac. HOWEVER, I highly recommend using the command-line tools for everything, and ignoring the GUI. I will not be providing help with configuring/using the GUI.
4. Clone your repo from github to your computer. When you are at the web page for your repo, `https://github.com/[your github id]/01_Git_and_Intro`, you will see info about how to clone it. The easiest way is to go to the command line terminal, and type `git clone git@github.com:[your github id]/01_Git_and_Intro.git`
5. Checkout your personal branch from the repo. Each student has a branch labeled by their Miami uniqueid. `git checkout uniqueid` ... for example, I would do `git checkout brinkmwj`
6. Complete the exercises below by modifying this file.
7. After you complete each answer, be sure to create a new commit with the changes (using `git add README.md` and `git commit -m` as appropriate). Also, be sure to upload to github frequently by using `git push`
8. If I don't see at least 4-5 commits on this homework, I'm going to be unhappy.
9. Once complete, send me a pull request. You should send from your branch in your github repo, to your branch in the MiamiOH-CSE274 repo. This is your official "turn in" of the homework, which I will grade.
10. Double check that you did the right thing by going to https://github.com/MiamiOH-CSE274/01_Git_and_Intro/pulls and making sure that your pull request is there, and looks like you expect. Optimism is the root of all evil.

Exercises
=========

#### 1. Based on the reading in the Git book, is it okay to keep your local copy of your repo on a USB drive and just carry it around? Explain why or why not. What about keeping it on the M: drive?

According to the book it is okay, and even advized to do so.  Git is made to work with all types of file paths so this won't cause any problems.
It is of course a good idea to have a physical copy as well as a copy on GitHub.  If either crash for some reason you have a back up.  Also if
you are unable to access the internet you still have the ability to work on your project, as long as you have a physical copy.  You just need to make sure
you later push these changes to GitHub so you have them there as well. 

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should clone your repository from your online GitHub and work on it from the computer you are using, it is fine not to have your flash drive.  Just
make sure you push frequently so you have the work when you go home.  Also when you use your flash drive again make sure you pull the
work that was newly added to GitHub to the work on your flashdrive. 

#### 3. Morin, Exercise 1.1 (p. 23)

[Your answer here]

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Your answer here]

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob is a binary representation of what is inside of a file.  It can be anytype of file.  In Git
this is how all files are stored so it is not limited to certain file types.
2. tree - A tree is the directory information for a blob.  A tree can reference another tree not just a blob
and therefor can create a huge hierarchy.  Git uses this to store and reference Blobs.
3. commit - A commit is the metadata for each change that is made.  A commit references the tree object and its current state when the 
commit is made.  Therefor commits create many trees all pointing to specific points in time when the commit was made.  Git uses this
to track changes. This allows you to go back to a certain point in your work before you made certain changes.  Its a great way to see
your work progress, and or go back to a point in time to avoid a new bug you may have coded.
4. repo - A repo is the main object in a project.  It holds all the branches of a project.  Git uses it to store each project and keep track of each branch of
the project.  A repo tends to be the main object which holds all of your changes and different branches.
5. hash - A hash is a 40 char hexidecimal string which references your blob.  This allows an extremely high number of files to be referenced and each be unique.
If a change is made to a file the file gets a new hash, therfor you can see the old file before the change, and after the change by 
referencing the hash value.  This allows Git to have imuteable objects.  