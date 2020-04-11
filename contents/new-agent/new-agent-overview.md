# Creating a New Virtual Assistant

In this lesson begins the process in which you will build a virtual agent from the ground up.

This virtual agent will build upon knowledge obtain in previous lessons to create a people management
virtual assistant. We also introduce some additional topics that permit the customization of the response based
on the specific user interacting with the virtual assistant.

The high level tasks needed to create this new virtual assistant are the following:

1. Create a new agent.
2. Defined User Properties 
3. Create a dictionary that maps terms
4. Setup response filters
5. Create tags
5. Create a Q&A Skill and Dialog Skill

Additional details about the steps follow below.

## Create a New Agent

In previous exercises we copied an existing agent which contained skills and then modified the agent to change
or add additional behavior. This time we are going to start with a blank agent and develop new skills for
this agent.

## Configure User Properties

User Properties are the method by which you can characterize specifics of an individual user. User properties
are then incorporated into a response filter to select a personalized response by the agent.

## Defined a Dictionary

Dictionaries permit the ability to map to  a standard term or word from their respective alternates. For example,
_leave_ _or _holiday_ is alternate to the more formal _PTO_(Paid Time Off). Dictionaries help with the
training aspect of intents by providing standard utterances. In the specific example _I want to take leave_
becomes equivalent to _I want to take PTO_.

## Configure Response Filters

Response filters provide the capability to provide a specific response agent response based upon a specific
user property, an entity, or custom criteria. A rudimentary example is one in which a defined user property such
as _location_ is set to Germany or USA based upon where the user resides. Using the value of _location_ a
specific response from the agent such as _How long have you lived Germany?_ or
_How long have you lived in the USA?_ can be formulated.

## Define Tags

Tags are used to classify specific intents and are recorded by the analytics engine to provide the specific
interaction of a user with the agent. So for example if you have configure an intent that relates to dental
coverage, and another that relates to vision coverage, one can tag each of these intents with the name
`Benefits` so that when any of these two intents are invoked the tag `Benefits` is logged with the intent.
A later time you can use query insights and filter on the specific tag `Benefits` to observe the intents
triggered by each.

## Develop a Q&A Skill and Dialog Skill

In previous lessons we have learned how to create Q&A and Dialog skills. We create additional skills of
these types for the new agent.

## Lesson 1: Create a New Agent

- Navigate to the agents dashboard and click on the _New Agent_ button which then displays a dialog.

- Provide a name in the _Agent name_ and a description in the _Agent description_ field as shown here:

![New agent dialog](contents/new-agent/images/new-agent-dialog.png)

- Click on the _Create Agent_ button to create the new agent.

![New agent](contents/new-agent/images/new-agent-landing.png)

## Lesson 2: Add an Avatar to the Agent

**TBD: Add steps for adding the avatar or refer to previous section**


You now have the base agent so we can move to the next step.



