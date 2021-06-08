---
title: The data dictionary
nav: Data Dictionary
topics: Survey structure; Data dictionary; 
description: REDCap can export and import the data structure for your project into a CSV-formatted file called a data dictionary. This is helpful for saving the design of your survey, or alternatively for rapidly building and importing a long survey with many questions. 
---

The easiest way to see how they work is to export one and look at it in Excel.

{% capture exportdict %}
1.	In the `Designer`, click the `Data Dictionary` tab.
2.	Click `Download the current Data Dictionary`. A CSV file titled `[Project Name]_DataDictionary_[Date].csv` will download to your `Downloads` directory.
3.	Locate the downloaded file and double-click it to open it in Excel. 
4.	Walk through the columns, noting especially the formatting of multiple choice options and calculated fields.
5.	In a new line, enter the following 
    Variable: prize; Form Name: prize_draw; Field Type: radio; Field Label: What reward would you like?; Choices: 1, Gift card | 2, Chocolates | 3, Movie tickets. 
6.	Save the file (in CSV format, if prompted by Excel).
{% endcapture %}
{% include card.html header="Export and edit a data dictionary" text=exportdict %}

{% capture uploaddict %}
7.	In the `Data Dictionary` tab, click `Upload a Data Dictionary`. 
8.	Navigate to your CSV file and select it for upload.
9.	Click on the `Online Designer` tab.
10.	Observe that a new instrument has been created called Prize Draw.
11.	Open the Prize Draw instrument and note the multiple choice field that was added by the uploaded data dictionary.
{% endcapture %}
{% include card.html header="Upload a data dictionary" text=uploaddict %}

___

{% include alert.html text="**All done here?** Move to the [next page](6-distribution.html)." color="success" %}