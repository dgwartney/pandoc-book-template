## Dictionaries

We are going to create three different dictionaries to map the location specific terms
for PTO or Paid Time Off. The dictionaries will come to play when train our Q&A
skill in later lessons.

### Exercise: Adding a new Dictionary

In this exercise you will create the global or default dictionary

- Navigate to **Agent -> Configuration -> Dictionaries**

![Dictionaries configuration](contents/hr-agent/images/dictionary-builder.png)

\pagebreak

- Click on the button _Add new_ button.

- Complete the dialog that is displayed as shown below:

![Creating a global dictionary](contents/hr-agent/images/global-dictionary-dialog.png)

\pagebreak

- Click on the _Create_ button to create the dictionary.

![New global dictionary](contents/hr-agent/images/global-dictionary-blank.png)

\pagebreak

- Add the values as shown here and then click on the _Save_ button:

![New global dictionary](contents/hr-agent/images/global-dictionary-save.png)

- Click the _Exit_ button to return to the list of dictionaries

\pagebreak

### Exercise: Add Specific Dictionaries for Asia, Europe, North America

Adding dictionaries for Asia, Europe, and America are performed similarly.

- Create the remaining dictionaries with values below where:

* Name/Description: `Americas`
    - Response Filters
        - `Location - United States`
        - `Location - Mexico`
        - `Location - Costa Rica`
    - Value
        - `PTO`
    - Synonyms
        - `Vacation`
* Name/Description: `Asia`
    - Response Filters
        - `Location - Japan`
    - Value
        - `PTO`
    - Synonyms
        - `Leave`
* Name/Description: `Europe`
    - Response Filters
       - `Location - Belgium`
       - `Location - Finland`
       - `Location - France`
       - `Location - Germany`
       - `Location - Ireland`
       - `Location - Poland`
    - Value
        - `PTO`
    - Synonyms
        - `Holiday`

