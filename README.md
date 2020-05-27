# Udacity Deep Learning Nanodegree (2020)


# LICENCE to Udacity

This repository contains materials which are owned and operated by Udacity. Most of the notebooks, many images and links in course note are from Udacity. Papers, reference applications, supplementary readings, materials are referred or linked in Udacity's Deep Learning Nanodegree lectures. Please refer to [Udacity DLN official Github repository](https://github.com/udacity/deep-learning-v2-pytorch) for the recent updates.


# Program Structure 

The Deep Learning Nanodegree program is divided into six parts:

1. Introduction to Deep Learning
2. Neural Networks
3. Convolutional Neural Networks
4. Recurrent Neural Networks
5. Generative Adversarial Networks
6. Deploying a Model


# GitHub LFS

Some files in this repository are large files which are larger than 50 MB. So I used `git lfs` to submit those files.

How to upload large files using LFS:
```
# go to the root directory of repository

git lfs install
git lfs track [LARGE_FILE_PATH]  # LARGE_FILE_PATH can include wildcard
git add [LARGE_FILE_PATH]
git add .gitattributes   # this file records which file is recorded by git lfs
git lfs ls-files  # check if LARGE_FILE_PATH is included
git commit -m "COMMIT MESSAGE"
git lfs push --all origin  OR  git push origin master
```

LFS References :

1. [Install git lfs](https://developer.lsst.io/v/DM-7674/tools/git_lfs.html#git-lfs-tracking)

2. [Resolving Git Large File Storage upload failures](https://help.github.com/en/github/managing-large-files/resolving-git-large-file-storage-upload-failures)

3. [About Git Large File Storage](https://help.github.com/en/github/managing-large-files/about-git-large-file-storage)

4. [Ignore tracking and Uploading large files](https://towardsdatascience.com/uploading-large-files-to-github-dbef518fa1a)

5. [Removing files from Git Large File Storage](https://help.github.jp/enterprise/2.11/user/articles/removing-files-from-git-large-file-storage/)

