---
title: Data collection instruments
nav: Instruments
topics: Instruments; forms; surveys; validation; 
---

## Designing data collection instruments


{% capture surveys %}

{% include alert.html text="REDCap considers anything that can capture data to be an ‘instrument’." color="info" %}

There are two ways to add data to an instrument: **forms** and **surveys**. They use the same fields and record the same data into the same database. The only difference is that forms are for you, and surveys are for your participants. Provided surveys have been enabled for your project, you can turn any form into a survey.

{% endcapture %}

{% include card.html header="Instruments v Forms v Surveys" text=surveys img="instruments-forms-surveys.png" %}

{% include figure.html img="instruments-forms-surveys.png" alt="Instruments, forms and surveys." width="75%" %}

# Designing your first instrument

You'll see one instrument in the list, called 'My First Instrument'.

{% capture text %}
**Rename your first instrument**    

1. Click on `Choose actions` under `Instrument actions` and select `Rename`.
2. Name the instrument *Demographic data*.
{% endcapture %}
{% include card.html header="Rename your first instrument" text=text %}

Now We’ll build a form and then turn it into a survey.

**Add two text fields**

1. Click on `My First Instrument`
2. Click `Add Field`
3. Choose `Text Box`
4. In the `Field` Label, type *Family Name* (this gets displayed to your participants)
5. In the `Field` Name, type *name_family* (this gets stored as a column header in your database)
6. In the `Required` field, select “Yes”.
7. In the `Identifier?` Field, select “Yes”. (Identifiable information can be flagged so as to remove it from exports.)
8. Click `Save`.
9. Repeat the process to add the field Given Name (name_given)

**Add a multiple-choice field**

1. Click `Add field`.
2. Choose `Multiple choice - Radio buttons` from the drop-down list.
3. Type *Gender* in the `Field` Label and *gender* in the `Variable Name`.
4. Add the following options: *Male, Female, Intersex, Unspecified*.
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

