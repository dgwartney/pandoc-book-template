# Lesson 1: Getting Started

This is the first paragraph of the introduction chapter.

## Exercise 1.1: Cloning a Sample Agent

Pick the Sample Agent, Sample Agent: My Assistant. Make a copy of the Agent by clicking the
hamburger menu and select the option - _Make a Copy_

![Making a copy of a sample agent](images/ch1/dashboard-make-copy.png)

## Exercise 1.2: Asking questions to the Agent

Now that your agent is ready, try asking some questions and see how it responds.

In your agent (Sample: My Assistant) try asking these questions:

````
I want to order a medium cheese pizza

What is the weather like in Seattle?

I want to see some general news

What's the stock price of Microsoft?
````

You can even use misspellings, try these examples:
````
I want to oder a pizza

What is the weater like in Seattle?

I want to general nws?

If the agent is not sure what you are asking about it responds with a disambiguation question. Try these examples to see the behavior:

I want to order a smed piza?

I wnt to se news?

Wht the stck pice of Microsft?
````

## Exercise 1.3: Changing the Agent Avatar and Name

## Exercise 1.4: Welcome and Returning User Messages

### Changing the Welcome Message

To change the welcome message you can click the Greeting in the built-in skills section.
Once you are in the greeting message, delete the text output and then add a card. In the description section of the card, add a short welcome message to your agent. For example:


### Returning User Message

You can configure a different message for users who are returning to use the Agent. In this section, we will set up a different welcome message for a returning user.
You can write a JavaScript code in Returning User Message handler that is executed when returning user accesses the agent and the returning value is sent as agent response.
To get to the Returning User Message navigate to Configuration -> Setting
Add the following code to Returning User Message handler:

```javascript
return [{
    quick_reply: {
        "content": "Hello " + context.user.first_name + " Would you like help with any of the following?",
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

## Exercise 1.5: Entity Types

In the Agent menu, click Entity types to observe and see the entities that the Agent is using.

In our example we see that the agent is using the following entities:

- Pizza Size

- Pizza Toppings

- US cities

- US States

- Stock Symbol

- Stock Name

Let’s try to edit some entity types and add some alternate values.
Click the entity type Pizza Size and add value - Extra large. Our agent will
now understand that extra large is a pizza size. To this extra-large entity
type add alternate values as shown below.

![Entities](images/ch1/dashboard-make-copy.png)

## Exercise 1.6: Deploying your Agent to a Web Page
