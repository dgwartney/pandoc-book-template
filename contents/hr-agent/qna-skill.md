## Q&amp;A Skill

You will now create a skill that will be able to answer frequently asked questions with varied
responses depending on which country the user is located.

### Exercise: Create a New Dialog Skill

Follow these steps to create the Q&A skill.

- Navigate to **Agent -> Skills**

![Skills Page](contents/hr-agent/images/qna-skill-page.png)

\pagebreak

- Click on the _Add Skill_ button

![Create skill type](contents/hr-agent/images/qna-skill-type-page.png)

\pagebreak

- Place you mouse over the _Q&A_ card and click on the _Create_ button.

- A dialog is displayed, fill in the values as shown below and click on the _Create_ button.

![Create Q&A skill dialog](contents/hr-agent/images/qna-create-dialog.png)

\pagebreak

- The Q&A skill builder is then shown.

![New Q&A Skill](contents/hr-agent/images/qna-skill-builder-page.png)


### Exercise: Import the Questions & Answers

To populate the Q&A skill with question/answers you will import them using a CSV file.

The pre-populated CSV file can be found [here](https://gitlab.com/david.gwartney/avaamo-tutorial-assets/-/raw/master/human-resources-faq.csv)

- Navigate to the Q&A skill you just created.

![Q&A skill builder page](contents/hr-agent/images/qna-skill-builder-page.png)

\pagebreak

- Click on the _Import_ button which displays the import dialog

![Q&A import dialog](contents/hr-agent/images/qna-import-dialog.png)

\pagebreak

- Click on the _Import_ button and locate the downloaded file from the link provide above 

![Q&A imported file](contents/hr-agent/images/qna-imported-file.png)

\pagebreak

- Click on the _Submit_ button to complete the import

- Lastly click on the _Save_ button to save the skill

### Exercise: Add the Response Filters and Tags to the Response

There are now 3 questions imported with 10 responses. The next step is to associate the response filters
with each of the responses.

The following shows how to attach a response filter to a specific response:

- Click on the intent `2020 Holidays`

- Click on second response marked with a _2_

![Q&A intent dialog](contents/hr-agent/images/qna-intent-dialog.png)

\pagebreak

- Click in the _Response Filter_ field and type `Belgium` which will locate the `Location - Belgium` response filter.

![Q&A intent dialog](contents/hr-agent/images/qna-intent-response-filter-belgium.png)

\pagebreak

- Select the response filter name in the popup.

![Q&A intent dialog](contents/hr-agent/images/qna-intent-response-filter-belgium.png)

- Click in the _Tags_ field and type `Belgium` which will locate the `Belgium` tag and select the tag name
in the popup

- Click in the _Tags_ field and type `Europe` which will locate the `Europe` tag and select the tag name

- Repeat the same steps above for each of the response filters using the list below. When completed
click on the _OK_ button. Next click on the _Save_ button in the upper right hand corner of the page.

* Response `3`
    - Response Filter
        - `Cost Rica`
    - Tags
        - `Costa Rica`
        - `Americas`
* Response `4`
    - Response Filter
        - `Finland`
    - Tags
        - `Finland`
        - `Europe`
* Response `5`
    - Response Filter
        - `France`
    - Tags
        - `France`
        - `Europe`
* Response `6`
    - Response Filter
        - `Germany`
    - Tags
        - `Germany`
        - `Europe`
* Response `7`
    - Response Filter
        - `Ireland`
    - Tags
        - `Ireland`
        - `Europe`
* Response `8`
    - Response Filter
        - `Japan`
    - Tags
        - `Japan`
        - `Asia`
* Response `9`
    - Response Filter
        - `Mexico`
    - Tags
        - `Mexico`
        - `Americas`
* Response `10`
    - Response Filter
        - `Poland`
    - Tags
        - `Poland`
        - `Europe`


### Exercise: Use the Skill

Try some example questions to the test out the skill:

>> _What are our holidays this year?_
>>
>> 



