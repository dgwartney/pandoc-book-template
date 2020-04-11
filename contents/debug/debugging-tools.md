# Debugging Tools

After completing the exercises in the lesson you will be able to:

- Use logging to troubleshoot code
- Viewing JavaScript errors

Exercise 1: Logging troubleshoot code

You can use `console.log()` to log errors and monitor these errors while testing the agent.
Lets see how to add a `console.log()` a message and see it in the debug logs.

Navigate to your order pizza skill in my assistant agent:

- In the first node of the dialog skill add a message to the console.

- Add a JS node in  the first node and add the following code:
`console.log("Hello World! This is my first console.log")`

- Navigate to your Agent-> Debug-> Debug log. This will open the debugging log on the left side of the screen.
Test your agent and your console.log() statement will appear in the debugging logs.
