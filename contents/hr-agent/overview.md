## Creating a Human Resources Agent

In this lesson begins the process in which you will build a Human Resources agent from the ground up.

This lesson will build upon knowledge obtain in previous lessons to create the agent.
We also introduce some additional topics that permit the customization of the response based
on the specific user interacting with the agent.

### Overview

The high level tasks needed to create this new agent are the following:

1. Create the new agent.
2. Defined _User Properties_
4. Setup _Response Filters_
3. Create a _Dictionary_ that maps terms
5. Create Tags to identify specific or groups of intents
5. Create a _Q&A Skill_ and _Dialog Skill_

Additional details about the steps follow below.

#### Create a New Agent

In previous exercises we copied an existing agent which contained skills and then modified the agent to change
or add additional behavior. This time we are going to start with a blank agent and develop new skills for
this agent.

#### Configure User Properties

User Properties are the method by which you can characterize specifics of an individual user. User properties
are then incorporated into a response filter to select a personalized response by the agent.

#### Configure Response Filters

Response filters provide the capability for the agent to provide a specific response based upon a 
user property, an entity, or custom criteria. A rudimentary example is one in which a defined user property such
as _Location_ is set to India or USA based upon where the user resides. Using the value of _Location_ a
specific response from the agent such as _How long have you lived in India?_ or
_How long have you lived in the USA?_ can be formulated.

#### Create Dictionaries

Dictionaries permit the ability to map to a standard term or word from their respective alternates. For example,
_leave_ or _holiday_ are alternative to the more formal _PTO_(Paid Time Off). Dictionaries help with the
training aspect of intents by providing standard utterances. In the specific example _I want to take leave_
becomes equivalent to _I want to take PTO_.

#### Define Tags

Tags are used to classify specific intents and are recorded by the analytics engine to provide additional
classification of the interaction of a user with the agent. So for example if you have configure an
intent that relates to dental coverage, and another that relates to vision coverage,
one can tag each of these intents with the name `Benefits` so that when any of these two intents are invoked the
tag `Benefits` is logged with the intent. A later time you can use query insights and filter on the specific tag 
`Benefits` to observe the intents triggered by each.

#### Develop a Q&A Skill and Dialog Skill

In previous lessons we have learned how to create Q&A and Dialog skills. You will create additional skills of
these types for the human resources agent





