# Getting Started

This initial section will have you replicate an existing virtual agent 
and after completing the exercises in the lesson you will be able to:

- Duplicate an existing virtual agent
- Ask questions of the agent
- Change the agent avatar and name
- Customize the welcome and returning user message
- Modify entity types
- Deploy an agent to a web page

## Exercise 1: Cloning a Sample Agent

Pick the Sample Agent, Sample Agent: My Assistant. Make a copy of the Agent by clicking the
hamburger menu and select the option - _Make a Copy_

![Making a copy of a sample agent](images/ch1/dashboard-make-copy.png)

## Exercise 2: Asking questions to the Agent

Now that your agent is ready, try asking some questions and see how it responds.

In your agent (Sample: My Assistant) try asking these questions:

>> _I want to order a medium cheese pizza_
>>
>> _What is the weather like in Seattle?_
>>
>> _I want to see some general news_
>>
>> _What's the stock price of Microsoft?_

You can even use misspellings, try these examples:

>> _I want to oder a pizza_
>> 
>> _What is the weater like in Seattle?_
>> 
>> _I want to general nws?_

If the agent is not sure what you are asking about it responds with a disambiguation question. Try these examples to see the behavior:

>> _I want to order a smed piza?_
>> 
>> _I wnt to se news?_
>> 
>> _Wht the stck pice of Microsft?_

## Exercise 3: Changing the Agent Avatar and Name

Click the edit icon (pencil) next to the agent name on the top left corner. The following pop-up is displayed,
where you can edit agent name and description:

![Change the agent name](contents/getting-started/images/change-agent-name.png)

## Exercise 4: Changing the Welcome Message

To change the welcome message you can click the Greeting in the built-in skills section.
Once you are in the greeting message, delete the text output and then add a card.
In the description section of the card, add a short welcome message to your agent. For example:

![Greeting Message](contents/getting-started/images/change-agent-name.png)

## Exercise 5: Changing the returning User Message

You can configure a different message for users who are returning to use the Agent. In this exercise,
we will set up a different welcome message for a returning user.
You can write a JavaScript code in Returning User Message handler that
is executed when returning user accesses the agent and the returning value is sent as agent response.

To get to the Returning User Message navigate to **Configuration -> Settings**

![Returning User Message](contents/getting-started/images/returning-user-message-settings.png)

Copy the following code and add to the returning user message handler:

```javascript
return [{
    quick_reply: {
        "content": "Welcome back " + context.user.first_name + ", would you like help with any of the following?",
        "links": [
            {
                "title": "Order a pizza",
                "type": "post_message",
                "value": "Order a pizza"
            },
            {
                "title": "Get weather",
                "type": "post_message",
                "value": "Get weather"
            },
            {
                "title": "Check stock prices",
                "type": "post_message",
                "value": "Check stock prices"
            },
            {
                "title": "Get news",
                "type": "post_message",
                "value": "Get news"
            }
        ]
    }
}];
```

## Exercise 6: Entity Types

In the Agent menu, click _Entity types_ to observe and see the entities that the Agent is using.

In our example we see that the agent is using the following entities:

- Pizza Size
- Pizza Toppings
- US cities
- US States
- Stock Symbol
- Stock Name

Let’s try to edit some entity types and add some alternate values.

Click the entity type Pizza Size and add value - Extra large. Our agent will now understand that extra large is a pizza size.

To this extra-large entity type add alternate values as shown below.

![Entity Types](contents/getting-started/images/entity-type-builder.png)

Save the changes, and build your agent. In the Agent simulator now ask, I want to order an extra large pizza_.
Your Agent will now understand the size extra large and ask you to select a topping.

![Testing entity types](contents/getting-started/images/entity-type-chat.png)

## Exercise 7: Testing your Updated Entities

Now that we have made so many changes to our Agent, open up the Agent Simulator and ask some questions.
Try incorporating the new entity types in your queries to see if the agent is able to understand the changes you have made.


## Exercise 8: Deploying your Agent to a Web Page

To user your Agent on the web navigate to **Agent -> Configuration -> Channel**.

![Agent Channels](contents/getting-started/images/channels.png)

Find the web channel in the page and click on the _view_ link:

![Web Channel Settings](contents/getting-started/images/web-channel-settings.png)

Click on the _test_ button which will open the agent on a new page. Click the avatar in the lower
right corner to interact with agent via the chat window.

![Testing the agent on the web](contents/getting-started/images/web-test-channel.png)

