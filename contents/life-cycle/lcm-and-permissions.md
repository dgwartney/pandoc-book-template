# Life-Cycle Management and Agent Permission

**TBD: Add graphics and clean up text and validate**

After completing the exercises in the lesson you will be able to:

- Understand how life-cycle management is implemented on the platform
- Understand and know how to use agent permissions

## Exercise 1: Understanding Life-Cycle Management
Typically the agent goes through different stages in its lifecycle right from the time of its inception
to the time it is pushed into production. Agents typically follow Development, Testing, Staging, and production.
In the new Avaamo 5.0, you can create users with different roles for collaborating in each stage of the agent lifecycle. 
This allows teams to develop, test, stage and deploy agents in a different environment,
thereby providing the required compliance.

### Development
Users with development roles gather requirements, configure the development environment, start designing and developing agents and skills as well as agents. The developers can also create copies of the agent and then prepare the agent for testing for the testing team.

### Testing
Users with a testing role testers can promote agents from development to testing environment, configure the test environment, test the agent’s functionality and report bugs and issues. Once testing is complete they notify the staging users, to promote the bot from testing to staging.

### Staging
Users with the staging role can promote the agents from testing to staging, configure the staging environment, test the agent’s functionality by replicating production instance, report bugs and issues. Staging users can also pull updates from testing to staging for re-testing the issues reported.

### Production
Users with the production role can promote agents from staging to the production environment. Production users can configure the production environment and report bugs and issuers in the live production instance. Production users can also pull updates from staging to production and also apply hot-fixes to the production if and when necessary.

### Reference Documentation
[See Plan your development process agent life cycle in the Avaamo documentation portal](https://docs.avaamo.com/v5/how-to/plan-your-development-process-agent-life-cycle)

Along with these stages, you can assign different roles to the users, to assign different roles:

- Log into user profile
- Grant roles such as Development, Testing, Staging and Production

**Note** You can only give access to the users if you have the setting role assigned.
If you don’t have the setting role then contact your admin.

![**TBD: Add Graphic**](contents/dialog/images/tbd)

![**TBD: Add Graphic**](contents/dialog/images/tbd)

![**TBD: Add Graphic**](contents/dialog/images/tbd)

Exercise 2: Understand Agent Permission

When you create an agent, you become the owner of the agent. Also, when a user promotes an agent,
he becomes the owner of the agent. As the owner of the agent, you can now assign different permissions
to different people within your company.

There are 4 types of permissions available for the agent:

- _View_ - Users can only view the agent, but cannot edit it
- _Edit_ - The users can view and edit the agent
- _Publish_ - Users can view agent, edit agent and publish skills from the agent to the skill store
- _Owner_ - Full access to the agent. Users can view agent, edit agent, publish agent from the agent to skill store, and edit agent permissions.

To give users permission to access your agent navigate to **Agent -> Configuration -> Permission**

You can read more about Permissions here: 
[https://docs.avaamo.com/v5/how-to/build-agents/configure-agents/permissions](https://docs.avaamo.com/v5/how-to/build-agents/configure-agents/permissions)

[https://docs.avaamo.com/v5/how-to/manage-platform-settings/users-and-permissions](https://docs.avaamo.com/v5/how-to/manage-platform-settings/users-and-permissions)

