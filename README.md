# About Project

This initiative is an integral part of the Codetopia community's open-source projects. Its primary objective is to provide you with insights into our approach to contributing across various projects within the Codetopia community's open-source ecosystem. While this guide is tailored for the current project, its applicability extends to all endeavors under the Codetopia community's open-source umbrella.

It's essential to note that this guide doesn't prescribe a rigid set of rules; instead, it serves as a flexible framework to assist you in initiating contributions to open-source projects. We encourage an open exchange of ideas and improvements for this project, as well as for any other initiatives within the Codetopia community. Your input is valued, and we welcome suggestions or enhancements.


**Table of content**
- [Pre-requisites](##pre-requisites)
- [Contributing to the project](##contributing-to-the-project)
    - [Make a copy first](###make-a-copy-first)
    - [Clone the repo](###clone-the-repo)
    - [Create an upstream](###create-an-upstream)
    - [Check up on upstream](###check-up-on-upstream)
    - [Create a branch](###create-a-branch)
    - [Work on the project](###work-on-the-project)
    - [Push to your origin](###push-to-your-origin)
    - [Create pull request](###create-pull-request)
- [Other resources](##other-resources)


## Pre-requisites

> Skip this section if you already have the following 
>
>- [git installed](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
>- [ssh setup with github](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)


In order to use git and also contribute to this project and other open-source projects, you need to install git on your local machine. You can check if you have git installed on your machine by running the following command in your terminal:

```bash
git --version
```

if you have git installed, you should see the version number. If you don't have git installed, you will need to [install](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) it on your local machine.

After installing git, you will need to [setup](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) ssh with github. This is because github now recommends users to use the ssh instead of **https**.

You can go through some [git tutorials](https://git-scm.com/book/en/v2) to get familiar with git.


## Contributing to the project
### Make a copy first

So you found a project you want to contribute to. Great! The first thing you should do is make a copy of the project. This is called **forking**. Forking is a way to make a copy of a repository under your own account. This allows you to make changes to the project without affecting the original project. It also allows you to make changes to the project without having to ask permission from the original project owner. You can fork a project by clicking the fork button in the top right corner of the project page.

1. Fork the repo from the main account into your own account by clicking on **fork**.

![forking repo](/images/fork.png)

2. Create the fork

![creating fork](/images/create-fork.png)

3. After creating the fork, you will be redirected to your own forked repo. You can verify that you are in your own forked repo by checking the top left corner of the page. It should say your username instead of the main account's username and you should see a message that says **forked from ...** with the main account's username.

![forked repo](/images/forked-link.png)

### Clone the repo
> before you continue with this step, you need to setup [ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) with github if you haven't already. This is because github now recommends users to use the ssh instead of **https**. 

Now that you have a copy of the project under your own account, you can clone it to your local machine. Cloning is a way to download the project to your local machine.
1. You can clone a project by clicking the green **Code** button, **SSH** and click the copy button to copy the URL.

![clone repo link](/images/code-url.png)

2. After copying the URL, open your terminal and navigate to the directory where you want to clone the project. Then run the following command:

```bash
git clone <url>
```

### Create an upstream
After successfully cloning the repo, you will need to create an upstream. An upstream is a way to connect your local repo to the original repo. This will allow you to pull in changes from the original repo into your local repo. But first, you will need to get the URL of the original repo.

1. Go to the original repo. or if you are already in your forked repo, click on the **forked from ...** link in the top left corner of the page to go to the original repo and copy the URL. 

![original url link](/images/original-url-link.png)

2. After copying the URL of the original repo, go to your terminal and navigate to the directory of the cloned repo. Then run the following command to create an upstream:

```bash 
git remote add upstream <orignal_repo_url>
```

3. To verify that you have successfully created an upstream, run the following command:

```bash
git remote -v
```
This will show you the origin and upstream URLs.

![remote urls](/images/remote-list.png)

The origin URL is the URL of your forked repo and the upstream URL is the URL of the original repo.

### Check up on upstream

To make sure that your local repo is up to date with the original repo, you will need to pull in changes from the original repo into your local repo. To do this, run the following command:

```bash
git pull upstream main
```

This will pull in latest changes from the original repo into your local repo. This is important to do before you start working on the project to make sure that you are working on the latest version of the project.


### Create a branch

If you have the latest version of the project, you can now create a branch. A branch is a way to make changes to the project without affecting the main branch. This is useful if you want to work on a feature or fix a bug without affecting the main branch. To create a branch, run the following command:

```bash
git switch -c <branch_name>
```

This will create a new branch and switch to that branch. You can verify that you are in the new branch by running the following command:

```bash
git branch
```

This will show you all the branches in the repo. The branch with the asterisk next to it is the branch you are currently in.

![branch list](/images/branch-list.png)

### Work on the project

After getting the latest version of the project, creating and switching to a new branch, you can now work on the project. 

### Push to your origin

After you are done working on the project, you will need to add and commit your changes to the new branch. To do this, run the following commands:

add your changes
```bash
git add .
```

commit your changes
```bash
git commit -m "your commit message"
```

and finally push your branch to your origin

```bash
git push origin <branch_name>
```

### Create pull request

After pushing your branch to your origin, you can now create a pull request. A pull request is a way to ask the original repo owner to pull in your changes into the main branch. To create a pull request, go to your forked repo and click on the **Compare & pull request** button.

![pull request button](/images/compare-pull-request.png)

After clicking the button, you will be redirected to the pull request page. Here you can review your changes and add a description of your changes. After reviewing your changes, click on the **Create pull request** button.

![create pull request](/images/create-pull-request.png)

After creating the pull request, you will be redirected to the pull request page. Here you can see the status of your pull request. If the pull request is approved, your changes will be merged into the main branch. If the pull request is not approved, you can make changes to your branch and push the changes to your origin. The pull request will automatically update with the new changes.

Now you have successfully contributed to an open-source project. Congratulations!

## Other resources
- [Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Git documentation](https://git-scm.com/doc)
- [Git tutorial](https://www.atlassian.com/git/tutorials)
- [The git book](https://git-scm.com/book/en/v2)
- [How to write a good commit message](https://chris.beams.io/posts/git-commit/)
- [How to write better commit messages](https://www.freecodecamp.org/news/writing-good-commit-messages-a-practical-guide/)
- [How to level up your git commit message](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)