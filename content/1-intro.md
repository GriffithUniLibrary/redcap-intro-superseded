---
title: Setting up your project
nav: Setup
---

# 1-Navigating

# Creating a new Project

**Create a new Project**

1. Click New Project in the REDCap main menu
2. Type Vaccine efficacy study into the Project name field
3. Note that changing the purpose of the project to “Research” allows you to enter some extra information about the research project. This has little practical effect on the project and can also be done after the project has been created.
4. Set the purpose to “Practice/Just for fun”.
5. Click Create Project.

# Setting up

The simplest way to get set up is to work down through each stage in the Project Setup tab.

## Main project settings

**Turn on surveys for your project**

1. Enable Use Surveys in this project. Without this, you can't create a survey instrument.
2. Explain that We won't be using longitudinal data collection in this workshop
3. Note that project title and purpose can also be changed here.
4. Click I'm done!
5. Show that each section displays Complete! once the I’m done! button is clicked.

# Designing data collection instruments

## Instruments v Forms v Surveys

REDCap considers anything that can capture data to be an ‘instrument’.

There are two ways to add data to an instrument: **forms** and **surveys**. They use the same fields and record the same data into the same database. The only difference is that forms are for you, and surveys are for your participants. Provided surveys have been enabled for your project, you can turn any form into a survey.

![Text, application

Description automatically generated](file:///var/folders/fh/w9vkbxsx4cg3gjc9s02blb380000gn/T/com.lukilabs.lukiapp/importD1742204-F14C-4CD8-890A-83A360A27A84.png)

# Designing your first instrument

You'll see one instrument in the list, called 'My First Instrument'.

{% capture text %}
**Rename your first instrument**    

1. Click on Choose actions under Instrument actions and select Rename.
2. Name the instrument Demographic data.
{% endcapture %}
{% include card.md header="Rename your first instrument" text=text %}

Now We’ll build a form and then turn it into a survey.

**Add two text fields**

1. Click on My First Instrument
2. Click Add Field
3. Choose Text Box
4. In the Field Label, type Family Name (this gets displayed to your participants)
5. In the Field Name, type name_family (this gets stored as a column header in your database)
6. In the Required field, select “Yes”.
7. In the Identifier? Field, select “Yes”. (Identifiable information can be flagged so as to remove it from exports.)
8. Click Save.
9. Repeat the process to add the field Given Name (name_given)

**Add a multiple-choice field**

1. Click Add field.
2. Choose Multiple choice - Radio buttons from the drop-down list.
3. Type Gender in the Field Label and gender in the Variable Name.
4. Add the following options: Male, Female, Intersex, Unspecified.
5. When you leave the field, REDCap automatically enters numerical raw values for each option.

Note here that the ‘raw value’, which appears before the column, is the value that gets recorded to your data. Thus your recorded value can be numeric, or a single letter code, while the participant can read a fuller description.

## Validation

We can apply validation for certain types of text entries. For example, we can make sure that a phone number or email address is correctly formatted.

**Add a postcode (validated)**

1. Click Add field.
2. Choose Text box.
3. Type Postcode in the Field Label and type postcode in the Variable Name.
4. In the Validation field, select Postal code (Australia). This will ensure only four numerals can be entered into the field.
5. In the Field note field, type “Providing your postcode is optional. We collect approximate residency data to assist with interpreting trial results.”
6. Click Save.

**Add an email (validated)**

1. Click Add field.
2. Choose Text box.
3. Type Email in the Field Label and type email in the Variable Name.
4. In the Validation field, select Email. This will ensure only correctly formatted emails can be entered into the field.
5. In the Identifier field, select “Yes”.
6. In the Field note field, type “Providing your postcode is optional. We collect approximate residency data to assist with interpreting trial results.”
7. Click Save.
8. Click Return to list of instruments.

## About identifiers

REDCap allows for personally identifiable information to be automatically removed from reports and exported data. Any field can be marked as an identifier.

REDCap uses the US HIPAA model to list what are likely to be personally identifying data. You can look it up using the REDCap help. It is a starting point and it likely to be similar to the Australian model.

However if you are collecting personal information from participants you should refer to the Privacy Principles found in the *Privacy Act 1988* (Cth) and Griffith’s Privacy Plan (see [https://www.griffith.edu.au/about-griffith/corporate-governance/plans-publications/griffith-university-privacy-plan#research](https://www.griffith.edu.au/about-griffith/corporate-governance/plans-publications/griffith-university-privacy-plan#research)).




`workshop-template-b` is a Jekyll project to create a simple workshop website, with a [Bootstrap](https://getbootstrap.com/)-based theme, designed for hosting on [GitHub Pages](https://pages.github.com/).

It works best for about 5 pages of instructions, plus index, all written in Markdown. 
The navigation to the main pages is exposed at top and bottom of each page for easy stepping through the lessons.

### Why?

Rather than making slides for a workshop, why not make a website? 
It's easier to write, access, share, and reuse. 
GitHub and GitHub Pages makes this pretty easy.

It is a better [Open Educational Resource](https://en.wikipedia.org/wiki/Open_educational_resources) since anyone can make a copy and adapt!

## GitHub Pages 

One amazingly useful GitHub feature is [GitHub Pages](https://guides.github.com/features/pages/).
It provides free static web hosting from any repository.
Gh-pages is intended to host relatively simple sites for your GitHub portfolio, project, or documentation.
Because it is free and a valuable transferable skill, this is a great option for teaching and learning.

Many organizations are using GitHub to collaboratively create and publish public workshop websites. 
For example: 

- [Programming Historian](http://programminghistorian.org/)
- [Software Carpentry](https://software-carpentry.org/), [Data Carpentry](http://www.datacarpentry.org/), [Library Carpentry](https://librarycarpentry.org/)
- this site!

{% capture text %}Note:
There are *soft* limits and guidelines for gh-pages usage: sites should be < 1GB, use < 100GB bandwidth per month, and make < 10 builds per hour.
If your site exceeds these quotas, GitHub will send you a notice asking you to modify the repository.
All content must follow the [community guidelines](https://help.github.com/articles/github-community-guidelines/), e.g. no violence, obscene sex, or illegal stuff.{% endcapture %}
{% include alert.html text=text color=secondary %}
