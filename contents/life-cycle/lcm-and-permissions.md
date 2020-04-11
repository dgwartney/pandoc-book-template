# Life-Cycle Management and Agent Permission

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
