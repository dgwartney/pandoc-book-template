# Language Support

After completing the exercises in the lesson you will be able to:

- Add a new language to an agent

- Understand how you can override the default translation of the added language

## Exercise 1: Adding a Language to an Agent

Open an agent and navigate to the **Agent-> Configuration -> Language**:

![Agent language configuration](contents/language/images/agent-language-configuration.png)

Click on the Add language button in the Language page which then displays a pop-up menu as shown here:

![Agent language configuration](contents/language/images/language-add-spanish.png)

In the search text field type: Spanish. Next select the menu item _Spanish (es-US)_ to select the US dialect
of the Spanish language.

Save the agent. Open the agent chat window and type the following: `#switch_langage es-US`.
You can now interact with the agent in the Spanish language.

Use Google Translate to formulate Spanish questions from English like the following example (Using the My Assistant agent):

_Order pizza_ => _Ordenar pizza_

## Exercise 2: Overriding Default Language Translation

Existing output to the user is automatically translated but can be overridden by different
responses in the added language. First you need to add the language to the dialog skill.
In this example we are using the **Order Pizza** skill. Adding a language is done similarly to the agent.
Open the skill, navigate to **Configuration -> Language**.
Add the language in the same manner as the previous exercise. Save the skill.

Navigate to the Implementation page and click on node 1. A dialog is then displayed. Click on the drop down menu that is showing English (US) and select the item Spanish (es-US). Spanish text is translated from English text by default. You can now override the Spanish as needed. 
