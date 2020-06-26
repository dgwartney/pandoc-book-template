## Building an Answers Skill

After completing the exercises in the lesson you will be able to:

- Create an Answers skill
- Uploading a PDF and creating an answers skill
- Understanding how to use the knowledge section of the answers skill
- Uploading a URL and creating an answers skill
- Learning how to train your skill

### Exercise: Create an Answers Skill

- In the Agent page, navigate to the Skills option in the left navigation menu and click _Add skill_.

- In the Skill builder page, select Answers and click Create.

- Specify Skill name: Credit Card Policy and Skill description: FAQs related to credit card policy and click Create.

![Create Answers skill dialog](contents/my-agent/answers/images/create-answer-skill-dialog.png)

### Exercise: Uploading a Document

In the Answers skill page, click _Add documents_ in the Documents tab. Click _Select files_, choose a PDF document,
and click the _Import_ button.

![Uploading a document](contents/my-agent/answers/images/uploaded-document.png)

Once the document is uploaded, and the training is completed,
your Answers skill is now ready for use.

![Trained document](contents/my-agent/answers/images/uploaded-document.png)

![Sample questions in chat window](contents/my-agent/answers/images/answers-chat-window.png){ width=250px }

In the Agent page, click the agent avatar in the bottom-right corner. You can now ask questions to see
if you are receiving appropriate responses. Click _View More_ to view the actual section in the document.
All the conversations are stored in the answer history and you can view the same to fine-tune the skill.

Here are some example questions:

>> _What is the late payment fee?_
>>
>> _What is the penalty fee?_

### Exercise: Examining Avaamo Answers Knowledge

To navigate to the knowledge goto **Answer Skill -> Implementation -> Knowledge**

To understand Answers better, click on the _Knowledge_ menu item in the skill menu.
The knowledge page consists of five tabs:

- Sections
- Entities
- Acronyms
- Vocabulary
- Knowledge graph

#### Sections

Sections are chunks of content extracted and created based on the structure of the uploaded document.
Each section contains the skill’s response to the user’s intent.
You can add additional training data as required.
Each section is displayed with a breadcrumb that indicates the page number from which the section is extracted and
the corresponding section header.

Navigate to the _Sections_ tab and observe the sections that have been identified.

![Answer skill sections](contents/my-agent/answers/images/answers-section.png)

#### Entities

Entities are business terms in your document. All entities are identified and extracted from your document
and classified as entities in this section. Here, you can either view all the entities from all the documents
or select a specific document and view all the entities.

![Answer skill entities](contents/my-agent/answers/images/answers-entities.png)

You can change the document by selecting the document from the dropdown in the top right corner of the page.
Select an entity from the list and try adding all the values.
Test this in the agent to see how it responds

#### Acronyms

If there is an acronym used in your document, then the acronym along with the full form is present in the acronyms tab.
Here, you can view all the acronyms available in the document.
You can get the definition of an acronym, like in the following examples:

>> _What is APR?_
>>
>> _What is DPR?_


![Answer skill acronyms](contents/my-agent/answers/images/answers-acronyms.png)

#### Knowledge Graph

This is a view only graph that maps the relationship between words. This mapping is based on the document uploaded,
the content and context of the document.

#### Resources

[View and Edit Knowledge in Avaamo documentation Portal](https://docs.avaamo.com/v5/how-to/build-skills/create-skill/using-avaamo-answers-1/manage-avaamo-answers-1/view-and-edit-knowledge)

### Exercise: Building an Answers Skill from a URL

Here we learn how to build an answers skill by providing a publicly accessible URL. 

- Create a answers skill as we have done previously with the _Skill name_ `Microsoft Support`
and _Skill description_ `Answer Skill for Microsoft Office Support`

![Creating the _Microsoft Office Support Answers_ skill](contents/my-agent/answers/images/answers-ms-support.png)

- In the Answers skill page, click on the button _Add URL_ in the Documents tab. In the popup, provide the URL,
a name for the URL and click the button Import URL.

- Once the import is successful and training is complete,
your Answers skill is now ready for use.

For the ease of understanding, the URL being used in this module is
https://support.office.com/en-us/article/put-a-background-picture-on-your-slides-7a17358c-b76e-4c94-84db-604e1bba76da.
You can either use this URL or use any other publicly available URL.

Here are some example queries to try with the URL provided above:

>> _Adding a background picture_
>>
>> _Pictures on slides_
>>
>> _Putting a background image on a slide_

