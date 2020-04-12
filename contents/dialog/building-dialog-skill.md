# Building a Dialog Skill

After completing the exercises in the lesson you will be able to:
- Identify and create Entity Types
- Create a Dialog Skill and adding training phrases to the invocation intent
- Create a conversation flow
- Learn how to capture data along with the flow of the conversation
- Learn how to add JavaScript files and perform simple API integrations
- Test your dialog skill using the Agent simulator
- Deploy your agent on the web channel

Let's build a skill to create an incident using a service now integration. Here are some ways people can ask the agent to create a ticket

>> _I want to create a support ticket_
>>
>> _My printer is not working, create a ticket_
>>
>> _My Desktop is laggy, raise an incident_
>
For the purpose of this exercise we are limiting the training to these 3 phrases,
you can go in and add more training data.

## Exercise 1: Creating a Dialog Skill

To create a new dialog skill:

- In the Agent page, click on the Skills option in the left navigation menu to display the Skills page.
Click on the _Add skill_ button.

- In the Skill builder page, select Dialog skill and click _Create_.

- Specify the following details and click the _Create_ button: 

## Exercise 2: Creating a Conversation Flow

I will be using a sample ServiceNOW instance for my integration here.
The mandatory fields to create a ticket are Short description, Description and Urgency. 
Our first node will be used to capture the short description, let's create the first node

[**TBD: Add Graphic**](contents/dialog/images/tbd)

Our Second node will be used to capture a detailed description of the issue reported. Let's create node 2.

[**TBD: Add Graphic**](contents/dialog/images/tbd)

Our third node will be used to capture the urgency of the ticket. Lets use a quick reply to show the urgency. The buttons will be:

- High
- Medium
- Low

Select post message option for each of the buttons added to quick reply

[**TBD: Add Graphic**](contents/dialog/images/tbd)

[**TBD: Add Graphic**](contents/dialog/images/tbd)

At the end your conversation tree will look like above.

Create a blank node 4, will be used to integrate with the service desk.

TIP: It's good to have validation for each node, for example you can check if the short description is too short,
or you can even check if the user entered the right urgency. You can use your validation code in post processing.

Documentation that describes how to create a new dialog is found at this link: https://docs.avaamo.com/v5/quick-start-tutorials/add-dialog-skill#step-1-create-new-dialog-skill-in-agent

## Exercise 5: Capturing Data from a Conversation

There are two ways to capture and store data from a conversation:
Using a JavaScript property context.variables.<variable_name> 
Using Javascript methods: Storage.user.set() to store and Storage.user.get() to retrieve.
For this example you will be using context.variables.<variable_name>. Context values are stored only along one single branch, if your conversation switches branches then the value is lost.

In the post-processing section of the document add this code for each node as shown below:

Node 2
Name: capture short description
Intent Type: Custom
Intent Code: return true
Post Processing: Yes
Post Processing Script:
context.variables.short_description = context.last_message;

[**TBD: Add Graphic**](contents/dialog/images/tbd)

Node 3
Name: capture description
Intent Type: Custom
Intent Code: return true
Post Processing Script:
context.variables.short_description = context.last_message;

[**TBD: Add Graphic**](contents/dialog/images/tbd)

Node 4
Capture Urgency
Intent Type = Custom
Intent Code: return true
Post Processing: Yes
Post Processing Script:
context.variables.short_description = context.last_message;

[**TBD: Add Graphic**](contents/dialog/images/tbd)

Exercise 5.6: Adding a JavaScript
Let’s add the javascript that will create the incident
You can add the following code to your code block:

**TBD: Provide this code so it can be in a JavaScript Include**
````javascript
var SERVICE_NOW_INSTANCE_ID = "66374";
var SERVICE_NOW_URL = "https://dev"+SERVICE_NOW_INSTANCE_ID+".service-now.com/api/now/";
var SERVICE_NOW_USERID = "admin";
var SERVICE_NOW_PWD = "qPoOh5VfCsV5";
let SERVICE_NOW_CALLER = "2def7d7edb3d330082fb6a49489619c0";

function createNewIncident(description,urgency,sht_desc) {
  let caller = SERVICE_NOW_CALLER;  
  let url = SERVICE_NOW_URL+'table/incident'
  return await(fetch(url, {
    method: 'POST',
    headers: {
      "Content-Type": "application/json",
      'Authorization': 'Basic '+Buffer.from(SERVICE_NOW_USERID+':'+SERVICE_NOW_PWD).toString('base64')
    },
    body: JSON.stringify({
      "short_description": sht_desc,
	  "caller_id": caller,
	  "description": description,
      "severity": 8,
      "impact": 9,
      "urgency":urgency
    })
  }).then(function(response) {
    return response.json();
  })
  .then(function(apiJson) {
    console.log(apiJson.result);
    return apiJson.result.number;
  
  }));
}


let shortDescription = context.variables.short_description
let description = context.variables.description
let urgency = context.variables.urgency

var incidentNumber = createNewIncident(shortDescription, description, urgency);
if(incidentNumber){ 
 return ("Ticket "+incidentNumber+" has been created on your behalf.");
}
else{
 return "Unable to create a ticket at the moment. Please try again later.";
}
````

Once the code has been written, save your changes to the skill and build the agent. Let's test the skill to see how it responds.

## Exercise 7: Exercise the Dialog Skill

Click the agent icon on the bottom right corner of the screen and ask the agent questions that you have trained it with.

[**TBD: Add Graphic**](contents/dialog/images/tbd)

## Exercise 8: Deploy your Agent on a Web Channel

To deploy your agent on a web channel, navigate to Agent Configure -> Channels 
Once in channels, click the view in the web channel card.

[**TBD: Add Graphic**](contents/dialog/images/tbd)

Click Test in the pop-up

[**TBD: Add Graphic**](contents/dialog/images/tbd)

Click on the Test button to view how your agent will appear in a web browser.
You can change the background of the webpage by using the parameter “&background = <publicly accessible image URL>”

