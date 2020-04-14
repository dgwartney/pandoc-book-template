## Creating a Human Resources Agent

In this lesson begins the process in which you will build a Human Resources agent from the ground up.

This lesson will build upon knowledge obtain in previous lessons to create the agent.
We also introduce some additional topics that permit the customization of the response based
on a specific user interacting with the agent.

### Overview

The high level tasks needed to create the human resources agent are:

1. Create a new _Agent_.
2. Define _User Properties_
4. Setup _Response Filters_
3. Create a _Dictionary_ that maps terms
5. Create _Tags_ to identify specific or groups of intents
5. Create a _Q&A Skill_ and _Dialog Skill_

Additional details about the steps follow.

**Create a New Agent**

In previous exercises we copied an existing agent which contained skills and then modified the agent to change
or add additional behavior. This time we are going to start with a blank agent and develop new skills for
this agent.

**Configure User Properties**

User Properties are the method by which you can characterize specific user. These user properties
are then incorporated into a response filter then used to select a personalized response by the agent.

**Configure Response Filters**

Response filters permit a specific response based upon a user property, an entity, or custom criteria.
A rudimentary example is one in which a defined user property such as _Location_ is set to Germany
or United States based upon where the user resides. Using the value of _Location_ a
specific response from the agent such as _How long have you lived in Germany?_ or
_How long have you lived in the United States?_ can be formulated.

**Create Dictionaries**

Dictionaries allow the ability to map to a standard term or word from their respective alternates. For example,
_leave_ or _holiday_ are alternative to the more formal _PTO_(Paid Time Off). Dictionaries help with the
training aspect of intents by providing standard utterances. In the specific example _I want to take leave_
becomes equivalent to _I want to take PTO_.

**Define Tags**

Tags are used to identify specific intents which are recorded by the analytics engine so as to provide additional
classification of the interaction of a user with the agent. For example, if you have tag an
intent that relates to dental coverage, and another that relates to vision coverage,
tagging each of these intents as `Benefits` so that when any of these two intents are invoked the
tag `Benefits` is logged with the intent. A later time you can use query insights to use 
`Benefits` to observe the set of queries that triggered these intents.

**Develop a Q&A Skill**

In previous lessons we have learned how to create Q&A. You will create an additional Q&A skill
for the human resources agent.





