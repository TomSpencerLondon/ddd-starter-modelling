### DDD starter modelling
This video is quite good for an overview of DDD starter modelling:
https://www.youtube.com/watch?v=qeir72soorI

The speaker Maxime Sanglan-Charlier refers to this repository:
https://github.com/ddd-crew/ddd-starter-modelling-process


![ddd-starter-modelling-process-colored](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/d0c739cd-a53a-4a9f-ab6e-42d81ae18308)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/eb256894-654a-4687-a329-c5c3aaeaff02)

#### Understand

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/cd68c777-9323-405f-bb6a-3c66bc01a227)

- Understanding of the domain

### What?
- The business model
- Users needs
- Value propositions

### Why?
- Any decisions should be aligned with business goals
- Share short, medium & long-term vision
- Give meaning to the team

![business-model-canvas](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/fd8823a8-8f57-42ca-b303-67b465586127)

A more focused tool could include the product vision board as focused on one product:
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/b8a21b94-b883-4b4e-ba9c-3e961ba28d5f)

Impact mapping is another tool for product oriented vision:
![Impact Mapping](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/8e0f36b1-5fe5-4bce-a6b4-8e0c41486e83)

The challenge with the above tools is to work out how to avoid merely tracking activity and ensure that there tasks are focused on the
usefulness of what teams are trying to deliver.

### Discover
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/eeaf937c-9c76-440c-a7fd-50a8b37a7d87)

### What?
- The domain
- The (ubiquitous) language, common vocabulary

### Why?
- Build a common ground
- Align all the stakeholders on the same level of understanding
- Put the puzzle together

#### Event Storming
Alberto Brandolini
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/fa373039-bf28-48e1-87cc-afac16f54713)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/c7dfc757-e439-4a5d-b863-cb2f246df21c)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/2098bbd6-20bf-440b-86e2-54d98b61cba1)

### User Story Mapping
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/0374571f-dfbc-4266-a925-bd5475a86a32)

### Domain Storytelling
https://egon.io/app/
https://github.com/WPS/egon.io-examples/tree/main

### Taxi example
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/322236ed-ae13-4d11-ac35-6f77059fea0e)

### cinema example
![metropolis-1-cinema-coarsegrained_2023-06-01](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/ce29c946-f58f-412d-93d4-096b25c67da9)

#### Web account
![request account for web app_2023-06-01](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/d751b01d-b8c6-4ff1-a03f-0264b93c5dbb)

### Decompose
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/bc64def7-dae5-44f1-bcd8-f24c014120a0)

#### What?
- The domain in sub domains

#### Why?
- Lowering cognitive load
- More autonomy
- High cohesion and low coupling
- Trace the architecture boundaries

https://microservices.io/patterns/decomposition/decompose-by-subdomain.html
![decompose-by-subdomain](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/1f66eebf-73f8-4e6e-83ef-97b0a3ff492d)

### Connect
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/ee6ee22d-6838-4e8b-96bb-bcbc1abd0d0c)

#### What?
- The sub domains

#### Why?
- Identify interactions and dependencies
- Validation through real use cases
- Better defined boundaries
- Find exchanged messages

https://github.com/ddd-crew/domain-message-flow-modelling

### Domain Message Flow Modelling

Designing loosely-coupled systems requires more than carefully designed boundaries. Carefully defined interactions between bounded contexts is equally important.

A [bounded context](https://martinfowler.com/bliki/BoundedContext.html) is a sub-system in a software architecture aligned to a part of the domain. It can be implemented as a microservice or a module within a monolith.

A Domain Message Flow Diagram is a simple visualisation showing the flow of messages (commands, events, queries) between actors, bounded contexts, and systems, for a single scenario.

### Separate Message & Contents

The separate message & contents format uses 2 shapes for each message: 1 for the name and order of the message and a separate box to display the contents of the message (the information it carries).

The benefit of this format is that you can focus on the flow of messages without getting bogged down by the message contents at the start.

Start by showing just the messages flowing between senders and receivers (with the order number on the message).

![just-messages-no-contents](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/c98019ca-99d3-4389-b9e5-2e45f5d61e81)

Then show the contents of each message in a separate box next to each message:

### Combined Message & Contents

The combined message & contents format uses a single shape to capture the message name, order, and contents.

![messages-and-contents](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/4f8b949e-d511-4ce4-b75f-39e1e23bf8a1)

![domain-message-flow](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/ab9bfb19-7fe3-4c54-85da-f4118f88c87c)

#### How to Use

When you have an initial cut of your architecture - you have identified candidate bounded contexts - you can begin design the message flows.

Start by creating a list of scenarios to model. And then for each scenario create a diagram

When creating a diagram, the typical flow is:

1. Start with an actor/context/system
2. Create the message they want to send
3. Add the recipient of the message and a line connecting the sender and the receiver
4. Place the message close to the line
5. Repeat steps 1 - 4 until your scenario is complete

The message should contain 3 elements:

1. The name of the message
2. The significant data contained within the message
3. The order in which the message occurs in the flow being modelled

#### Context mapping
This video from Michael Plod is quite useful on context mapping:
https://www.youtube.com/watch?v=VjtMt689ql8

"A loosely coupled software architecture and org structure to match" is a key predictor of:
- Continuous Delivery Performance
- Ability to scale organization and increase performance linearly

#### Patterns to describe the contact between bounded contexts and teams
- open / host service (shared API)
- conformist
- anticorruption layer
- shared kernel
- customer / supplier
- partnership
- published language
- separate ways
- big ball of mud

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/227196f2-7eb1-4701-8dce-9ee8b98945da)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/fed2e557-2e85-4d9a-8a66-b7c780ed2c04)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/a9191d8d-3a3c-481b-9b9e-8df85ff91258)

Context Maps aim to deliver a holistic overview regarding coupling of bounded contexts.

With context mapping we focus on dependencies between bounded contexts:
![context-map-cheat-sheet](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/321fe720-b55f-40ec-a9e4-80b17bc6bc58)

![context-map](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/e5095fb6-abd6-4e94-a2b8-f5b8d3ec4c51)
