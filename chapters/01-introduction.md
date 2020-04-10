# Lesson 1: 

This is the first paragraph of the introduction chapter.

## Exercise 1.1

This is the first subsection. Please, admire the gloriousnes of this seagull:

![A cool seagull.](images/seagull.png)

A bigger seagull:

![A cool big seagull.](images/seagull.png){ width=320px }

## Exercise 1.2

This is the second subsection.


Please, check [First: Images] subsection.

Please, check [this](#first-images) subsection.

| Index | Name |
| ----- | ---- |
| 0     | AAA  |
| 1     | BBB  |
| ...   | ...  |

Table: This is an example table.

## Exersize 1.3

Formula example: $\mu = \sum_{i=0}^{N} \frac{x_i}{N}$

Now, full size:

$$\mu = \sum_{i=0}^{N} \frac{x_i}{N}$$

And a code sample:

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


## Exercise 1.4: Welcome and Returning User Messages

### Change the Welcome Message

To change the welcome message you can click the **Greeting** in the built-in skills section.
Once you are in the greeting message, delete the text output and then add a card. In the description section of the card, add a short welcome message to your agent. For example:

![A cool seagull](images/seagull.png){#fig:seagull}


## Exercise 1.5: Entity Types


## Exercise 1.6: Deploying your Agent to a Web Page
