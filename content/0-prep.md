---
title: Getting Started
nav: Start
topics: GitHub; REDCap; LimeSurvey; Griffith; Research
---

# 0-Getting Started

# Accessing REDCap for the first time

The Griffith REDCap instance1 is hosted at [www151.griffith.edu.au/redcap/](https://www151.griffith.edu.au/redcap/). The simplest way there is via [griffith.edu.au/survey-centre](https://www.griffith.edu.au/survey-centre).

REDCap logins are connected to the Griffith phonebook using LDAP. Your Griffith s-number and password allow you to enter. There is no need to maintain separate login details.

Note: You'll be logged out if you are inactive for more than a certain period.

### Logging in to REDCap

1. Open a browser and using the search box to find the Research Survey Centre web page.
2. Log in to REDCap using your s-number and password.

## The My Projects screen

The My Projects screen shows any projects you are working on or have access to.

![Image](https://res.craft.do/user/full/7836f923-6db2-5fd7-3b84-3456dcff553c/doc/4E782528-E777-4CCA-8611-568A0FCE5611/72D01A0E-9DE9-4AFB-BF63-F0EBF30A8A21_2)

## Home Menu

### My Projects

The following headings can be seen:

- **Records:** how many records (complete or partial) have been recorded for this project. This doesn't distinguish between records captured by researchers completing a form and records captured by participants completing a survey instrument.
- **Instrument:** An instrument is how data gets captured into REDCap. They can either be forms (for researchers to complete inside of REDCap) or surveys (for participants to complete on their own devices).
- **Type:** The type may either be classic or modern. This category doesn’t change and is irrelevant.
- **Status:** Can be in development (the wrench symbol) or production (the green tick). Once a project is in production, it can also be set to inactive and archived statuses.

### New Project

Creates a new project.

### Help & FAQ

REDCap has an extensive, searchable help section built in. We encourage you to use it frequently.

### Send-It

Send-It is a secure file transfer application for sending recipients files up to 35 MB in size. We won’t be looking at it in this session.

### Messenger

REDCap includes a feature that allows you to send messages to your project collaborators within the web app. This could be useful where you want to keep conversations about your project in the same place as the project itself. We won’t be looking at it in this session.

### My Profile

You can set preferences relating to name, email address and regional number formats here.



To create your own materials using `workshop-template-b`, please create a free [GitHub account](https://github.com/join) if you do not have one already.
Basic familiarity with the GitHub web interface will be helpful.

For a quick introduction check out GitHub's [Hello World guide](https://guides.github.com/activities/hello-world/), or the extensive [GitHub Learning Lab](https://lab.github.com/).

It is possible to create a website with this template using only GitHub's web interface--in fact, it works great!
However, for more advanced uses you will want Git, Ruby, and Jekyll installed on your computer to do local development.

{% capture text %}
1. Have a [GitHub](https://github.com) account.
2. Click the green "Use this template" button on the [workshop-template-b repository](https://github.com/evanwill/workshop-template-b) to make your own copy.
3. Optional: have [Git](https://git-scm.com/), [Jekyll](https://jekyllrb.com/), and a nice [text editor](https://code.visualstudio.com/) installed.
{% endcapture %}
{% include card.html text=text header="Setup Overview" %}

# Local Jekyll Setup [optional]

## Install Git

[Git](https://git-scm.com/) is a [free](https://www.gnu.org/philosophy/free-sw.en.html), [distributed](https://en.wikipedia.org/wiki/Distributed_version_control) version control system. [GitHub](https://github.com/) is a Git repository hosting service, a place to store and sync your work in the cloud--your Jekyll and GitHub Pages projects will be under Git version control, so you need the software on your machine. 

- Windows: install [Git for Windows](https://git-for-windows.github.io/) using the default options. This will give you Git, Git Bash, and Git GUI. Git Bash is a great terminal that lets you use UNIX style commands on Windows.
- Mac: check if Git is already installed by opening terminal and typing `git --version`. If you do not have it, download the official [Mac installer](https://git-scm.com/downloads).
- Linux: check if Git is already installed by opening terminal and typing `git --version`. If you do not have it, install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).

If you are interested in using a visual GUI application integrated with GitHub, Windows and Mac users should also install [GitHub Desktop](https://desktop.github.com/) using the default options.
You can install GitHub Desktop in addition to other versions of Git.

There are other [GUI apps available](https://git-scm.com/downloads/guis) for managing and visualizing Git repositories, including Linux options.

## Install Ruby

[Ruby](https://www.ruby-lang.org/en/) is a fairly young and developing programming language with some unique features. 
To use Jekyll, you do not need to know anything about Ruby, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/).
Frustratingly, different versions have many dependency and incompatibility problems.
Because of these issues, many use Ruby Managers, such as [RVM](http://rvm.io/), to switch between versions.
However, if you are just interested in working with Jekyll, using an installer for your OS should be sufficient.
Jekyll requires a Ruby version > 2.2.5.

- **Windows:** Use [RubyInstaller for Windows](https://rubyinstaller.org/). 
    - First, [download](https://rubyinstaller.org/downloads/) the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.7.X (x64)) and double click to install. Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.
    - Second, the installer will open a terminal window with options to install MSYS2 DevKit components. Choose option 3, "MSYS2 and MINGW development toolchain", or simply press ENTER to install all the necessary dependencies. (This installer can be restarted by typing `ridk install` into a command prompt)
- **Mac:** OS X has a version of Ruby installed by default. Check the version with `ruby -v`. If it is > 2.2.5 you can use the system Ruby. However, a newer version can be installed using [Homebrew](https://brew.sh/), `brew install ruby`, or a manager such as [rbenv](https://github.com/rbenv/rbenv) or [RVM](http://rvm.io/). Check the official Jekyll [Mac install docs](https://jekyllrb.com/docs/installation/#macOS) for tips.
- **Linux:** Even though the version will not be the most up-to-date, the simplest method is to use your distro's repositories. For example on Ubuntu, `sudo apt install ruby-full`. Make sure the repository version is > 2.2.5. You will also need the build tools Make and GCC, on Ubuntu get them with `sudo apt install build-essential`. For a more up-to-date version, use a manager such as [RVM](http://rvm.io/).

## Install Jekyll

Jekyll is a Gem, a software package installed via Ruby's management system called RubyGems (similar to Python's Pip). 
Open a terminal and type:
`gem install jekyll bundler`

This will take a minute as Gem installs all the dependencies and builds extensions. 

# Text Editor

When working with code you should have a good text editor.
Windows notepad does not handle UTF-8 encoding or UNIX line endings that are standard for cross platform applications. 
For basic editing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient.
However, a more complete code editor will be helpful for managing Jekyll projects.

Open-source cross platform suggestions:

- [Visual Studio Code](https://code.visualstudio.com/)
- [Atom](https://atom.io/)
