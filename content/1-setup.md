---
title: Getting Started and setting up
nav: Setup
topics: Logging in; My Projects; Creating a project
description: Let's look at how to access REDCap for the first time. 
---

{% capture beforewebegin %}

{% capture planningalert %}

A significant amount of careful planning and design needs to happen before you start building your survey. The stronger your preparation, the more credible your methodology will be. 

{% endcapture %}
{% include alert.html text=planningalert color="warning" %}

Your **preparation** phase should have included:

- Research problem development
- Literature review
- Concept mapping and identification of measures
- Survey cohort identification

Your **design** phase should have included: 

- Clarifying the _answers_ you want (not the questions)
- Question design
- Question validation
- Sampling design

See this <a href="content/LowChoyResBaz2021.pdf">presentation</a> by Associate Professor Sama Low-Choy on the Survey Lifecycle.

{% endcapture %}

{% include card.html header="<i class='fa-solid fa-bomb'></i> Before we get started" text=beforewebegin %}

The Griffith REDCap instance is hosted at [www151.griffith.edu.au/redcap/](https://www151.griffith.edu.au/redcap/). You can also get information about REDCap and Lime Survey (Griffith's other supported survey solution) via the Library's [Working with Data](https://www.griffith.edu.au/library/research-publishing/working-with-data/create-and-capture) page.

REDCap logins are connected to the Griffith phonebook using LDAP. Your Griffith s-number and password allow you to enter. There is no need to maintain separate login details.

{% capture logoutwarning %}
**Note:** You'll be logged out if you are inactive for more than a certain period.
{% endcapture %}
{% include alert.html text=logoutwarning color="warning" %}

{% capture text %}

1. Open a browser and paste `https://www151.griffith.edu.au/redcap/` into the address bar.
2. Log in to REDCap using your s-number and password.
3. The first screen you will be shown is the `My Projects` screen. 

{% endcapture %}
{% include card.html header="Logging in to REDCap" text=text %}

___

## The My Projects screen

The `My Projects` screen shows any projects you are working on or have access to.

{% include figure.html img="my-projects.png" alt="Alt text" caption="REDCap Projects Screen" width="100" %}

### Home Menu


My Projects
: The page you are looking at

New Project
: Creates a new project.

Help & FAQ
: REDCap has an extensive, searchable help section built in. We encourage you to use it frequently.

Send-It
: Send-It is a secure file transfer application for sending recipients files up to 35 MB in size. We won’t be looking at it in this session.

Messenger
: REDCap includes a feature that allows you to send messages to your project collaborators within the web app. This could be useful where you want to keep conversations about your project in the same place as the project itself. We won’t be looking at it in this session.

My Profile
: You can set preferences relating to name, email address and regional number formats here.

--

The following headings can be seen in the list of projects:

Records
: how many records (complete or partial) have been recorded for this project. This doesn't distinguish between records captured by researchers completing a form and records captured by participants completing a survey instrument.

Instrument
: An instrument is how data gets captured into REDCap. They can either be forms (for researchers to complete inside of REDCap) or surveys (for participants to complete on their own devices).

Type
: The type may either be classic or modern. This category doesn’t change and is irrelevant.

Status
: Can be in development (the wrench symbol) or production (the green tick). Once a project is in production, it can also be set to inactive and archived statuses.

___

{% capture createnew %}

1. Click `New Project` in the REDCap main menu
2. Type _Vaccine efficacy study_ into the `Project name` field

{% include alert.html text="Note: changing the purpose of the project to “Research” allows you to enter some extra information about the research project. This has little practical effect on the project and can also be done after the project has been created." color="info" %}

3. Set the purpose to “Practice/Just for fun”.
4. Click Create Project.

{% endcapture %}
{% include card.html header="Create a new project" text=createnew %}

## Setting up

{% include alert.html text="The simplest way to get set up is to work down through each stage in the Project Setup tab." color="info" %}

{% capture projectsettings %}

**Turn on surveys for your project**

1. Enable Use Surveys in this project. Without this, you can't create a survey instrument.
2. Explain that We won't be using longitudinal data collection in this workshop
3. Note that project title and purpose can also be changed here.
4. Click I'm done!
5. Show that each section displays Complete! once the I’m done! button is clicked.

{% endcapture %}
{% include card.html header="Main project settings" text=projectsettings %}

___


{% include alert.html text="**All done here?** Move to the [next page](2-instruments.html)." color="success" %}