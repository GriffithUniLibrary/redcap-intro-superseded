---
title: Branching logic, stop actions and action tags
nav: Branching
topics: Branching; Stop actions; Action tags
---

### Branching logic

You can decide to show or hide specific questions based on the results of previous questions, including the results of calculated questions. Here, we are going to show a participant a warning about their BMI if it is over a certain value. 

{% include alert.html text="Branching logic cannot be tested until the survey is published." color="warning" %}
 
{% capture bmiwarning %}
1.	Click `Add field`.
2.	Choose `Descriptive Text` (with optional Image/Video) for the `Field Type`.
3.	In the `Field` Label, type the following:
    Based on the information you've provided, your BMI (body mass index) is in a range associated with increased risk of cardiovascular diseases and diabetes. 
4.	In the `Variable Name`, type bmi_warning.
5.	Click `Save`. 
6.	Click the `Branching Logic Button` ( ).
7.	Select the `Drag-N-Drop Logic Builder`. 
8.	Drag bmi = (define criteria) to the right column. 
9.	Select greater than (`>`) and type 30 in the value field. 
10.	Note that the equation `[bmi] > 30` also appears in the Advanced Branching Logic Syntax section above. 
{% endcapture %}
{% include card.html header="Create a BMI warning" text=bmiwarning %}


Stop Actions
You can end the survey automatically based on a participant’s answers to a question.
Stop Actions cannot be tested until the survey is published. 
Create a Stop Action
11.	Click Return to list of instruments.
12.	Choose the Baseline Health Data instrument.
13.	Scroll to the question that reads: Do you suffer from any of the following conditions?
Click the red   button in the question menu.
14.	Select Asthma and click Save. 
15.	Note that the Asthma option now has [End Survey] alongside it in red. 

Note that Stop Actions don’t support ending the survey based on multiple conditions (e.g. [Age] > 45 AND [Diabetes] = YES) but you may be able to achieve a similar result using a combination of Branching and Stop Actions.
Action tags
Action tags can help format or adapt entries automatically. For example they can limit the number of characters a participant enters in a field, or prevent them from selecting more than a certain number of options. 
Here we are going to create a ‘None of the Above’ checkbox option, that automatically unchecks all the other boxes, and unchecks itself if any other box is ticked. 
Add ‘None of the Above’ to the Existing Conditions’ question
1.	Click the edit button ( ) next to the question labelled Do you suffer from any of the following conditions? 
2.	Add a new option to the list of options as follows: 5, None of the above. 
3.	In the Action Tags field, type @NONEOFTHEABOVE=5. This indicates that the answer option coded as ‘5’ operates as the ‘none of the above’ option. 
4.	Note that we can only test this action tag by looking at the live survey, once it has been published.
