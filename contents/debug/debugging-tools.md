# Debugging Tools

**TBD Remove reference to My Assistant make this more of a reference**

After completing the exercises in the lesson you will be able to:

- Use logging to troubleshoot code
- View Javascript errors

## Exercise 1: Logging Within JavaScript Blocks

You can use `console.log()` to log errors and monitor these errors while testing the agent.
Lets see how to add a `console.log()` a message and see it in the debug logs.

Navigate to your order pizza skill in my assistant agent:

- In the first node of the dialog skill add a message to the console.

- Add a JavaScript response node in the first node and add the following code:
`console.log("Hello World! This is my first console.log")`

- Navigate to your **Agent-> Debug-> Debug log**. This will open the debugging log on the left side of the screen.
Test your agent and your `console.log()` statement will appear in the debugging logs.

![Javascript logging console](contents/debug/images/javascript-logging.png)

## Exercise 2: Viewing JavaScript Errors

You can view JavaScript errors from the agent dashboard. 

To view JavaScript errors navigate to **Agent -> Debug -> JS Errors**

In the agent My Assistant navigate to JS errors to see if you can find any errors in your agent.

![Javascript error log](contents/debug/images/javascript-errors-log.png)

[To learn more about debugging and loggin see _Using JS Errors_ from the Avaamo documentation portal](https://docs.avaamo.com/v5/how-to/build-skills/create-skill/using-dialog-designer/debug-skill#using-js-errors)
