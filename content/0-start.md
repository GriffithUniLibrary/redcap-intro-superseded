---
title: Getting Started
topics: GitHub; REDCap; LimeSurvey; Griffith; Research
description: Let's look at how to access REDCap for the first time. 
---

The Griffith REDCap instance is hosted at [www151.griffith.edu.au/redcap/](https://www151.griffith.edu.au/redcap/). You can also get information about REDCap and Lime Survey (Griffith's other supported survey solution) via the Library's [Working with Data](https://www.griffith.edu.au/library/research-publishing/working-with-data/create-and-capture) page.

REDCap logins are connected to the Griffith phonebook using LDAP. Your Griffith s-number and password allow you to enter. There is no need to maintain separate login details.

{% capture logoutwarning %}
**Note:** You'll be logged out if you are inactive for more than a certain period.
{% endcapture %}
{% include alert.html text=logoutwarning color="warning" %}

{% capture text %}

1. Open a browser and using the search box to find the Research Survey Centre web page.
2. Log in to REDCap using your s-number and password.
3. The first screen you will be shown is the 'My Projects' screen. 

{% endcapture %}
{% include card.html header="Logging in to REDCap" text=text %}

___

## The My Projects screen

The My Projects screen shows any projects you are working on or have access to.

{% include figure.html img="my-projects.png" alt="Alt text" caption="REDCap Projects Screen" width="100" %}

### Home Menu

> **My Projects:** The page you are looking at 

> **New Project:** Creates a new project.

> **Help & FAQ:** REDCap has an extensive, searchable help section built in. We encourage you to use it frequently.

> **Send-It:** Send-It is a secure file transfer application for sending recipients files up to 35 MB in size. We won’t be looking at it in this session.

> **Messenger:** REDCap includes a feature that allows you to send messages to your project collaborators within the web app. This could be useful where you want to keep conversations about your project in the same place as the project itself. We won’t be looking at it in this session.

> **My Profile:** You can set preferences relating to name, email address and regional number formats here.

--

The following headings can be seen in the list of projects:

- **Records:** how many records (complete or partial) have been recorded for this project. This doesn't distinguish between records captured by researchers completing a form and records captured by participants completing a survey instrument.
- **Instrument:** An instrument is how data gets captured into REDCap. They can either be forms (for researchers to complete inside of REDCap) or surveys (for participants to complete on their own devices).
- **Type:** The type may either be classic or modern. This category doesn’t change and is irrelevant.
- **Status:** Can be in development (the wrench symbol) or production (the green tick). Once a project is in production, it can also be set to inactive and archived statuses.

___

{% include alert.html text="**All done here?** Move to the [next page](1-setup.md)." color="success" %}