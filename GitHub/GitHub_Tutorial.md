Getting Around GitHub: Tutorial
================
Michelle Slawinski
3/6/2022

-   [Learning Objectives](#learning-objectives)
-   [Git](#git)
    -   [What is Git?](#what-is-git)
    -   [Set Up](#set-up)
    -   [Git Configuration Basics](#git-configuration-basics)
    -   [Help Options](#help-options)
    -   [Git Resources](#git-resources)
-   [Graphical User Interface (GUI)](#graphical-user-interface-gui)
    -   [What are GUIs?](#what-are-guis)
    -   [Popular GUIs](#popular-guis)
    -   [GUI Resources](#gui-resources)
-   [GitHub](#github)
    -   [What is GitHub?](#what-is-github)
    -   [Setup](#setup)
    -   [Let’s Practice](#lets-practice)
-   [RStudio](#rstudio)
    -   [Setup](#setup-1)
    -   [RStudio Resources](#rstudio-resources)
-   [Last Minute Things](#last-minute-things)
    -   [Dictionary](#dictionary)
    -   [Tips](#tips)

Git.. GitHub.. What are they? Why do they matter? In this tutorial we
will introduce you to them and provide you with the basics! This
presentation is for individuals with limited knowledge on git and
graphical user interfaces, although those with a robust background are
more than welcome to drop some knowledge on us! From one novice git user
to another, we will walk through it together.

# Learning Objectives

1.  Describe git and graphical user interfaces
2.  Set up and connect git, GitHub and RStudio
3.  Create your own profile repository on GitHub
4.  Practice navigating how to fork, commit, and request a pull on
    Github

# Git

## What is Git?

Have you ever tried working on a project or a specific piece of code
with a colleague but could not figure out what changes they made? Or
have you ever overwritten your own code and had to rewrite the chunk
from the beginning?

Frustrating, right? Well, git is a version control that allows you to do
better. Be a better coder, communicator and person because the time you
will save can then be spent elsewhere!

## Set Up

Let’s get started shall we!

First, check to see if you already have Git installed.

On Windows, look for an application called “Git Bash” and on Macs,
search for an application called “Terminal.” Type “git version” into the
terminal. If you receive a version number, Git is installed. However, if
the terminal is saying unknown command, then Git it not installed.

No Git? No problem. Navigate to [git](https://git-scm.com/) and click
*Downloads.* Select the software appropriate for your system and follow
the remaining installation steps.

**Windows**

1.  Select **“Click here to download”** This should be the version you
    need however, you can look below to see additional options.
2.  Allow installer to download then open.
3.  “Do you want to allow this app to make changes to this device?” Yes,
    yes you do! You will need administrative access to your computer for
    this.
4.  Use the defaults throughout the installation process.

**Mac**

If you have Git installed, then we will most likely just need to update
it. To update git follow this
[video](https://modulesunraveled.com/installing-git/updating-git-if-you-have-only-version-comes-xcode-or-command-line-developer-tools)!

Otherwise, to install git:

1.  Select **“Click here to download.”** This should be the version you
    need however, you can look below to see additional options.
2.  Click on the Binary installer link and select download.
3.  Once it is downloaded, open the file, locate the package, right
    click and select “Open.”
4.  Follow the prompts.
5.  For help with the remaining installation process, follow this
    [video](https://modulesunraveled.com/installing-git/installing-git-if-you-do-not-have-xcode-or-command-line-developer-tools-installed).

## Git Configuration Basics

When you configure git you will have options on what level you would
like to make configurations.

     System Level: git config --system

     User Level: git config --global

     Project Level: git config

Let’s set up some basic git configurations for our system.

1.  Username: When you set your user name using global, git will use
    this information for anything you do.
    -   git config --global user.name “Michelle Slawinski”
2.  Email: Do the same thing with your email address. This should be the
    email you used to set up your GitHub account. If you have not signed
    up for a GitHub account, do that now.
    -   git config --global user.email “my\_email.com”
3.  Viewing git configurations: Type this command and scroll to the
    bottom to see the configurations you set up.
    -   git config --list

For other configuration options see
[here](https://git-scm.com/docs/git-config).

## Help Options

Are you stuck? Ask Git! In the terminal, type “git help” and it will
return some common Git commands. If you want to learn more about a
specific command such as branching, you can type “git help branch” and
it will pull up a manual on branching.

![image](git%20help%20branch.PNG)

## Git Resources

-   [Pro Git Book](https://git-scm.com/book/en/v2)
-   [Git Reference Guides](https://git-scm.com/docs)
-   [GitHub Git Guides](https://github.com/git-guides/install-git)
-   [‘Awesome Git’ Repository](https://github.com/dictcp/awesome-git)
-   [LinkedIn Learning Git Essential Training: The
    Basics](https://www.linkedin.com/learning-login/share?account=42166124&forceAccount=false&redirect=https%3A%2F%2Fwww.linkedin.com%2Flearning%2Fgit-essential-training-the-basics%3Ftrk%3Dshare_ent_url%26shareId%3DSxKxywffQ8iDu%252FzDfk84uw%253D%253D)

# Graphical User Interface (GUI)

## What are GUIs?

Git but better. GUIs are where you can use Git but in a more visually
pleasing manner. Instead of using command lines in Git, you can use a
click-based GUI. Think of it like using R/SAS versus SPSS or Jasp.

## Popular GUIs

| Microsoft      | Mac            |
|----------------|----------------|
| GitHub Desktop | GitHub Desktop |
| GitKraken      | GitKraken      |
| Sourcetree     | Sourcetree     |
| TortoiseGit    | Fork           |
| \*SmartGit     |                |

## GUI Resources

-   [GUI Clients](https://git-scm.com/downloads/guis)
-   [GitHub Help](https://docs.github.com/en)
-   [GitKraken Support](https://support.gitkraken.com/)
-   [Sourcetree
    Support](https://confluence.atlassian.com/get-started-with-sourcetree)

# GitHub

## What is GitHub?

GitHub makes it easier on us as human beings! GitHub is a cloud based
management tool for your code. Think of it like Google Docs’ tracked
changes feature. In any document, you can use tracked changes to
*visualize* the changes you or someone else are making. In GitHub, we
are using a similar way to visualize version control. This is extremely
important when you start working in teams or on a large project. You
will want to have changes to your code saved so that you can refer back
if you need to.

## Setup

Navigate [here](https://desktop.github.com) to download GitHub Desktop
and follow prompts.

Note: You will want to create an account and hold on to the email you
use for this account.

## Let’s Practice

Now that you have an understanding of Git and GUIs such as GitHub, let’s
practice!

We will be practicing how to fork a repository from GitHub, make a
change locally, then commit those changes and push them back to GitHub.
Ready? Lets get our feet wet.

1.  Navigate to [RLadies of Gainesville’s
    GitHub](https://github.com/R-Ladies-Gainesville)
2.  Locate and click on the “practice” repository
3.  In the upper right hand corner, click “Fork” Once you have it
    forked, you will see that it is in your remote GitHub. Now that you
    have it remotely, we will want to get access to it locally so that
    we can add to the repository.
4.  Click into the ‘practice’ repository if you are not already in it
    and click on the ’Code" drop down.
5.  Select Open with GitHub Desktop. Once you click this, GitHub Desktop
    should open with a screen asking you where you would like to place
    the repository on your desktop. Go ahead and find where you would
    like to put the repository.

# RStudio

## Setup

``` r
library(usethis)
```

You should have the latest version of R and Rstudio downloaded. To check
your current version of R:

``` r
R.version.string
#> [1] "R version 4.0.5 (2021-03-31)"
```

You will also want to have git installed at this point. To introduce
yourself to git using RStudio:

``` r
use_git_config(user.name = "Michelle Slawinski", user.email = "slawinsm@gmail.com") 
  #use.email should be the same as your GitHub account
```

To configure GitHub with RStudio, you will need to set up a token in
RStudio. This is basically a secure connection between GitHub and
RStudio:

``` r
usethis::create_github_token()
#> * Call `gitcreds::gitcreds_set()` to register this token in the local Git credential store
#>   It is also a great idea to store this token in any password-management software that you use
#> * Open URL 'https://github.com/settings/tokens/new?scopes=repo,user,gist,workflow&description=DESCRIBE THE TOKEN\'S USE CASE'
gitcreds::gitcreds_set
#> function (url = "https://github.com") 
#> {
#>     if (!is_interactive()) {
#>         throw(new_error("gitcreds_not_interactive_error", message = "`gitcreds_set()` only works in interactive sessions"))
#>     }
#>     stopifnot(is_string(url), has_no_newline(url))
#>     check_for_git()
#>     current <- tryCatch(gitcreds_get(url, use_cache = FALSE, 
#>         set_cache = FALSE), gitcreds_no_credentials = function(e) NULL)
#>     if (!is.null(current)) {
#>         gitcreds_set_replace(url, current)
#>     }
#>     else {
#>         gitcreds_set_new(url)
#>     }
#>     msg("-> Removing credetials from cache...")
#>     gitcreds_delete_cache(gitcreds_cache_envvar(url))
#>     msg("-> Done.")
#>     invisible()
#> }
#> <bytecode: 0x0000000013dc6f60>
#> <environment: 0x0000000013d589f0>
```

## RStudio Resources

-   [An Introduction to Git and how to use it with
    RStudio](https://r-bio.github.io/intro-git-rstudio/)
-   [GitHub and
    RStudio](https://resources.github.com/whitepapers/github-and-rstudio/)
-   [Happy Git and GitHub for the
    useR](https://happygitwithr.com/connect-intro.html)

# Last Minute Things

## Dictionary

| Term           | Definition                                                                                                              |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
| Shell          | A terminal that uses written commands to interact with your operating system                                            |
| Git Directory  | Umbrella terms for all of your files and folders                                                                        |
| Modify         | Changed the file but have not committed it to your local system                                                         |
| Staged/Indexed | Marked a modified file to go into your next commit snapshot                                                             |
| Commit         | Save the state of your project in your local system                                                                     |
| Branch         | When you duplicate part of a repository                                                                                 |
| Merge          | After you finish updating the code you branched, you can merge it back into the project’s main source code              |
| Push           | Once you commit your project or file to your local system, you have the option to push it to remote GitHub              |
| Pull           | If your repository has new changes in GitHub, you can download and integrate those remote changes by using ‘pull’       |
| Fetch          | To see if there are remote changes, you can use fetch to see what was updated. Fetch will not merge your updates though |

## Tips

1.  Update some basic profile features GitHub offers like a picture,
    occupation, or location! Click your picture in the top right corner
    after logging in and select ‘Settings.’
2.  You can also personalize your profile’s ReadMe file with an
    introduction for people who will visit your page. This is again
    optional but helps you get noticed. If you want to see some super
    cool examples, beef up your profile with certain tools, or do some
    late night reading on how to make your profile stand out, look at
    this
    [repository](https://github.com/abhisheknaiidu/awesome-github-profile-readme)!
3.  Make sure you have a ReadMe file for every repository. This serves
    as an executive summary for your project and saves viewers time on
    figuring out what the purpose of your project is.
4.  When you make a commit, make sure you are descriptive, especially if
    you are working on a team. You can use git to search your commit
    messages so you’ll want to be descriptive! Google ‘git commit best
    practices’ and you can look through all the suggestions on how to do
    this.
5.  Branch this markdown file and add your own tips!

& that’s it!
