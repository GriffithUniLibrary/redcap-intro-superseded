---
title: Validations and calculations
nav: Validation
topics: Validation; Multiple choice; Calculated fields
description: 
youtubeid: 
---

You may wish to break your data gathering into several instruments. This way, you can present certain question groups only to specific cohorts, or at different times (e.g., at 0, 3 and 6 months). 

{% capture baseline %}
1.	Click `Create` a new instrument from scratch.
2.	Click `Add instrument here`
3.	Name your instrument _Baseline Health Data_.
{% endcapture %}
{% include card.html header="Create a Baseline health data instrument" text=baseline %}


### Validating dates

{% capture baseline %}
1.	Open the `Baseline Health Data` instrument
2.	Click `Add field`.
3.	Choose `Text box`.
4.	Type _Date of Birth_ in the `Field` description and type _dob_ in the `Variable Name`.
5.	In the `Validation` field, select _Date (D-M-Y)_. This will ensure only dates can be entered into the field.
{% endcapture %}
{% include card.html header="Add a Date of Birth field" text=baseline %}

### Validating numbers

{% capture heightweight %}
1.	Create two new text box fields:  for Height (cm) (Variable Name: __height_cm__) and Weight (Kg) (Variable Name: __weight_kg__) using the instructions above.
2.	For each one, set the `Validation` to _Integer_. This will ensure only numbers can be entered into the field.
{% endcapture %}
{% include card.html header="Add height and weight fields" text=heightweight %}

### Multiple choice fields

{% capture conditions %}
3.	Click `Add field`.
4.	Choose _Checkboxes (Multiple Answers)_ for the `Field Type`.
5.	In the `Field Label`, type _Do you suffer from any of the following conditions?_.
6.	In the `Variable Name`, type __pre_conditions__.
7.	In the `Choices Field`, type the following on separate lines:
- _Diabetes_
- _Cardiovascular disease_
- _Asthma_
- _Anxiety or depression_
8.	In the `Required` field, click _Yes_. 

{% include alert.html text="REDCap automatically adds numeric Raw Values for each choice. Raw values are what gets saved to the database when a participant chooses a value. You can change the raw values to something else if you want." color="info" %}
{% endcapture %}
{% include card.html header="Add a multiple choice field" text=conditions %}

### Calculated fields

You can use calculated fields to determine values based on the values of previous fields. Here we will determine the participant’s age and body mass index (BMI) based on their date of birth and their height and weight. 

{% include alert.html text="Calculated fields cannot be tested until the survey is published. " color="warning" %}


{% capture age %}
1.	Click `Add field`.
2.	Choose _Calculated Field_ for the `Field Type`.
3.	In the `Field Label`, type Y_our age at the start of this project_.
4.	In the `Variable Name`, type __age_at_start__.
5.	In the `Calculation Equation`, type: `datediff([dob],"2020-01-01","y")` 

{% include alert.html text="REDCap understands terms like ‘now’ and ‘today’, but they are not recommended for calculating age because they will lead to variation in values over time. This is why we select a set date such as January 1 or the project start date." color="info" %}
{% endcapture %}
{% include card.html header="Calculate the participant’s age" text=age %}


{% capture bmi %}
Here, we are going to use the 'height' and 'weight' values provided by the user to calculate their body mass index (BMI).

1.	Click `Add field`.
2.	Choose `Calculated Field` for the `Field Type`.
3.	In the `Field Label`, type Your Body Mass Index (BMI).
4.	In the `Variable Name`, type bmi.
5.	In the `Calculation Equation`, type: `[weight]*10000/([height]*[height])`.

REDCap understands many calculation functions you might be familiar with in Excel, including IF() statements. 

{% endcapture %}
{% include card.html header="Calculate the participant’s BMI" text=bmi %}

___

{% include alert.html text="**All done here?** Move to the [next page](4-branching.html)." color="success" %}