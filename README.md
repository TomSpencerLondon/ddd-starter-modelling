### DDD starter modelling
This video is quite good for an overview of DDD starter modelling:
https://www.youtube.com/watch?v=qeir72soorI

The speaker Maxime Sanglan-Charlier refers to this repository:
https://github.com/ddd-crew/ddd-starter-modelling-process

In this repo, I am trying to gather the resources mentioned and to give an overview of the different stages of the process
which the DDD crew, Maxime Sanglan-Charlier, Nick Tune and Michael Plod suggest can be useful in order to understand and build successful
Domain Driven architecture.


This diagram shows the different stages of the process. The stages move from a mile high context overview of the business 
moving down to a deeper understanding of the domain and business rules that make up the code:
![ddd-starter-modelling-process-colored](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/d0c739cd-a53a-4a9f-ab6e-42d81ae18308)

Here we can see that the different stages are grouped into broad areas. We have align and understand which 
means getting the vision of the project and understanding the business value. Strategic architecture describes how to 
group the events identified in the align and understand stage. In the strategy section, the emphasis is on how to direct team effort
towards sucessful domain development. This section also includes some work on Team Topologies and business strategy: 
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/eb256894-654a-4687-a329-c5c3aaeaff02)

Next we will look at each of the stages in turn and document the tools that we can use to enable good progress during each
stage:

#### Understand
First we look at the Understand stage. In this stage the challenge is to understand the business model and user needs.
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/cd68c777-9323-405f-bb6a-3c66bc01a227)

In this stage we are looking for an overarching understanding of the domain

### What?
- The business model
- Users needs
- Value propositions

### Why?
- Any decisions should be aligned with business goals
- Share short, medium & long-term vision
- Give meaning to the team

This tool looks quite interesting for understanding the key areas of the business. It does seem that it might be possible to use
this on a project level. The Key Partners might be collaborators for the project including other teams and companies, key activties
would describe the problem that the project solves. This business model canvas does seem quite high level for a developer.
![business-model-canvas](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/fd8823a8-8f57-42ca-b303-67b465586127)

A more focused tool could include the product vision board as focused on one product:
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/b8a21b94-b883-4b4e-ba9c-3e961ba28d5f)
I think this tool is a bit more focussed for developers and might be a better way for developer to understand the value that is
offered by the project.

Impact mapping is another tool for product oriented vision:
![Impact Mapping](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/8e0f36b1-5fe5-4bce-a6b4-8e0c41486e83)
Impact mapping is used by Gojko Adzic:
https://www.youtube.com/watch?v=ZgHkdJ6T8oQ
The main point here is that we are creating a map which is focussed on business goals. Here the developers are not necessarily
involved in ticket creation so it may be less important for developers to use this tool. The main point here is to gain context
so that ticket creators are able to clearly understand whether tickets are related to business goals.

The challenge with the above tools is to work out how to avoid merely tracking activity and ensure that there tasks are focused on the
usefulness of what teams are trying to deliver.

### Discover
The discover stage can include event storming and focusses on representing the domain visually and collaboratively.
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
User story mapping is another tool for relating tickets to high level tasks users can do in the product that
the project is implementing:
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/0374571f-dfbc-4266-a925-bd5475a86a32)

### Domain Storytelling
Domain storytelling is a tool for understanding the interactions that users have with the business.
This site is quite easy to use and can be a useful tool for understanding business processes in the application
teams are building:
https://egon.io/app/

https://github.com/WPS/egon.io-examples/tree/main

Here are a few domain storytelling examples for reference:
### Taxi example
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/322236ed-ae13-4d11-ac35-6f77059fea0e)

### cinema example
![metropolis-1-cinema-coarsegrained_2023-06-01](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/ce29c946-f58f-412d-93d4-096b25c67da9)

#### Web account
![request account for web app_2023-06-01](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/d751b01d-b8c6-4ff1-a03f-0264b93c5dbb)

### Decompose
The decompose stage is focussed on splitting the domain into sub-domains.
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/bc64def7-dae5-44f1-bcd8-f24c014120a0)

#### What?
- The domain in sub domains

#### Why?
- Lowering cognitive load
- More autonomy
- High cohesion and low coupling
- Trace the architecture boundaries

The below diagram is quite useful to visualise how a domain might be split into separate subdomains:
https://microservices.io/patterns/decomposition/decompose-by-subdomain.html
![decompose-by-subdomain](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/1f66eebf-73f8-4e6e-83ef-97b0a3ff492d)

### Connect
In the connect stage we are trying to use the subdomains we have identified to build a loosely coupled architecture:
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
- anti corruption layer (transforms data for use in the application)
- shared kernel (shared artifact between two teams, e.g. database)
- customer / supplier (downstream is the customer of the supplier(upstream))
- partnership (cooperative relationship between two teams)
- published language (e.g. calendar invites follow a published language .ics)
- separate ways (bounded contexts have no connections)
- big ball of mud (part of a system that is a mess)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/227196f2-7eb1-4701-8dce-9ee8b98945da)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/fed2e557-2e85-4d9a-8a66-b7c780ed2c04)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/a9191d8d-3a3c-481b-9b9e-8df85ff91258)

Context Maps aim to deliver a holistic overview regarding coupling of bounded contexts.

With context mapping we focus on dependencies between bounded contexts:
![context-map-cheat-sheet](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/321fe720-b55f-40ec-a9e4-80b17bc6bc58)
The focus is on how teams interact:
![context-map](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/e5095fb6-abd6-4e94-a2b8-f5b8d3ec4c51)

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/bee5f016-8908-484f-9cca-0de197b5a225)

### Strategise
This is the stage where teams can strategise using all the subdomains discovered with the above tools.

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/f015a5bd-9d0c-4312-ac66-0ac5aa98ff0c)

#### What?
- The sub domains

#### Why?
- Identify core sub domains
- Focus on what's important
- Build vs Buy
- Help to think short, medium and long-term

Teams would then place the different parts of the application in the correct places on the below graph:
![core-domain-chart](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/ae71f07f-c365-475a-9a40-fb3ad4e25628)
This would help them identify which tool is core for the business and which tools are supporting or generic.
- core - usp - unique selling proposition - make application different
    - cinema management - movies + cinemas
- supporting
    - anything that is required to perform business - but not core business
    - loyalty card - not required for core business but necessary to support business
- generic
    - supports business but generic to any business
    - invoicing

### Organise

![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/0eda8128-3f82-4d85-b6e6-f9a9e7c5f68c)

#### What?
- Teams

#### Why?
- Identify teams' dependencies and responsibilities
- Lower cognitive load
- Limit context switching
- Consider org constraints


![team-topologies](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/72fe29be-4675-4f7c-924e-d8dd3828f1c7)

![team-interaction](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/016fff81-840d-48db-b4dc-04a07095fc0e)

Each service must be fully owned by a team with sufficient cognitive capacity to build and operate it.

#### Cognitive load
Hacking Your Head Managing Information Overload
Jo Pearce
https://www.youtube.com/watch?v=DUlFxffjDFo

- intrinsic (how do I write a Java class)
- extraneous (how do I deploy this app)
- germane (business problems)

Manage intrinsic load, reduce irrelevant load, increase relevant load = Efficient learning and increased productivity

### Define
In the define stage teams would identify bounded contexts and aim to document the inbound and outbound communications
to and from the API.
![image](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/969b4f9c-caba-4bdf-a1e1-676d07e702f1)

#### What?
- purpose
- roles and traits

#### Why?
- Challenge the boundaries
- New perspective
- Documentation

![bounded-context-canvas-v5](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/f88cd15f-182b-4e75-a398-ff8270111d8c)

![BCCanvasExample](https://github.com/TomSpencerLondon/LeetCode/assets/27693622/4b6a8221-d1df-4505-a676-6214b978039b)


#### Using the C4 Model
The C4 model can also be a useful tool during the define stage.
The C4 diagram has four parts:
- System Context
- Container
- Component
- Code

For the moment we will focus on the first three parts of the C4 diagram. There are three main elements to the System Context
diagram:
- people
- Your software system (that you are designing)
- Supporting software systems

We will start by adding Nodes:

```mermaid
flowchart TD
    User["Premium Member
    [Person]
    A user of the website who has
    purchased a subscription"]
```

There are various options for the direction of the flowchart:
- TB: top-to-bottom
- TD: top-down
- BT: bottom-to-top
- RL: right-to-left
- LR: left-to-right

```mermaid
flowchart TD
    User["Premium Member
    [Person]
    
    A user of the website who has
    purchased a subscription"]
    
    LS["Listings Service
    [Software System]
    
    Serves web pages displaying title
    listings to the end user"]
    
    TS["Title Service
    [Software System]
    
    Provides an API to retrieve
    title information"]
    
    RS["Review Service
    [Software System]
    
    Provides an API to retrieve
    and submit reviews"]
    
    SS["Search Service
    [Software System]
    
    Provides an API to search
    for titles"]
    
    User--"Views titles, searches titles\nand reviews titles using" --> LS
    
    LS--"Retrieves title information from"-->TS
    LS--"Retrieves from and submits reviews to"-->RS
    LS--"Searches for titles using"-->SS
```

#### Adding Style

We can now add style to the nodes:

```mermaid
---
title: "Listing Service C4 Model: System Context"
---
flowchart TD
    User["🧍 
    Premium Member
    [Person]
    
    A user of the website who has
    purchased a subscription"]
    
    LS["Listings Service
    [Software System]
    
    Serves web pages displaying title
    listings to the end user"]
    
    TS["Title Service
    [Software System]
    
    Provides an API to retrieve
    title information"]
    
    RS["Review Service
    [Software System]
    
    Provides an API to retrieve
    and submit reviews"]
    
    SS["Search Service
    [Software System]
    
    Provides an API to search
    for titles"]
    
    User--"Views titles, searches titles\nand reviews titles using" --> LS
    
    LS--"Retrieves title information from"-->TS
    LS--"Retrieves from and submits reviews to"-->RS
    LS--"Searches for titles using"-->SS
    
    classDef focusSystem fill:#1168bd,stroke:#0b4884,color:#ffffff
    classDef supportingSystem fill:#666,stroke:#0b4884,color:#ffffff
    classDef person fill:#08427b,stroke:#052e56,color:#ffffff

    class User person
    class LS focusSystem
    class TS,RS,SS supportingSystem
```

#### MovieBooker System Context

```mermaid
---
title: "Listing Service C4 Model: System Context"
---
flowchart TD
    Admin["🧍 
    Administrator
    [Person]

    Administrator who
    updates MoviePrograms"]

    User["🧍‍♀️
    MovieBooker
    [Person]
    
    Movie Goer views programs 
    and makes bookings"]
    
    MB["Movie Booker
    [Software System]
    
    Serves web pages displaying title
    listings to the end user"]
    
    MS["MovieService
    [Software System]
    
    Provides an API to retrieve
    title information"]
    
    BS["Booking Service
    [Software System]
    
    Provides an API to retrieve
    and submit bookings"]
    
    MG["Movie Goer Service
    [Software System]
    
    Provides information
    about the current user
    for titles"]
    
    Admin--"Views users and updates programs" --> MB
    User--"Views titles, searches titles\nand reviews titles using" --> MB
    
    MB--"Retrieves title information from"-->MS
    MB--"Retrieves bookings from"-->BS
    MB--"Retrieves movie goer info from"-->MG
    
    classDef focusSystem fill:#1168bd,stroke:#0b4884,color:#ffffff
    classDef supportingSystem fill:#666,stroke:#0b4884,color:#ffffff
    classDef person fill:#08427b,stroke:#052e56,color:#ffffff
    classDef admin fill:#08427b,stroke:#052e56,color:#ffffff

    class User person
    class Admin admin
    class MB focusSystem
    class MS,BS,MG supportingSystem
```

#### Detail the System's Containers

For the Container diagram, the second level of the C4 diagrams, we can talk about further detail
for the containers that are in play:
- A mobile application for mobile users
- A web application that serves web browsers and also hosts an API for the mobile app to retrieve/send data to/from
- A Redis instance for caching, to prevent repeated API calls to downstream services, such as the title service

We also have a message broker in the form of Kafka, that we send domain events to when important things happen
such as when a user views listings or a user watches a title.

```mermaid
---
title: "Listing Service C4 Model: Container Diagram"
---
flowchart TD
    User["🧍 
    Premium Member
    [Person]
    
    A user of the website who has
    purchased a subscription"]
    
    WA["Web Application
    [.NET Core MVC Application]
    
    Allows members to view and review titles
    from a web browser. Also exposes
    an API for the mobile app"]
    
    MA["Mobile Application
    [Xamarin Application]
    
    Allows members to view and review
    titles from their mobile devices"]
    
    R[("In-Memory Cache
    [Redis]
    
    Titles and their reviews
    are cached")]
    
    K["Message Broker
    [Kafka]
    
    Important domain events
    are published to Kafka"]
    
    TS["Title Service
    [Software System]
    
    Provides an API to retrieve
    title information"]
    
    RS["Reviews Service
    [Software System]
    
    Provides an API to retrieve
    and submit reviews"]
    
    SS["Search Service
    [Software System]
    
    Provides an API to search
    for titles"]
    
    User--"Views titles, searches titles
    and reviews titles using\n[HTTPS]"-->WA
    
    User--"Views titles, searches titles
    and reviews titles using
    [HTTPS]"-->MA
    
    subgraph listing-service[Listing Service]
        WA--"Reads and writes to\n[Redis Serialization Protocol]"-->R
        MA
    end
    
    WA-."Publishes messages to\n[Binary over TCP]"..->K
    WA--"Makes API calls to\n[HTTPS]"--->TS
    WA--"Makes API calls to\n[HTTPS]"--->RS
    WA--"Makes API calls to\n[HTTPS]"--->SS
    MA--"Makes API calls to\n[HTTPS]"-->WA


    classDef container fill:#1168bd,stroke:#0b4884,color:#ffffff
    classDef person fill:#08427b,stroke:#052e56,color:#ffffff
    classDef supportingSystem fill:#666,stroke:#0b4884,color:#ffffff
    class User person
    class WA,MA,R container
    class TS,RS,SS,K supportingSystem
    style listing-service fill:none,stroke:#CCC,stroke-width:2px
    style listing-service color:#fff,stroke-dasharray: 5 5
    
```
This is a list of arrow types for mermaid diagrams:

![image](https://user-images.githubusercontent.com/27693622/230421778-650b4cf3-06d7-498f-8991-7dbd21842aeb.png)

#### Component diagrams
Often the System Context and the Container diagram are enough in terms of higher level architectural detail.
However, it can be useful at times to create a component diagram.

```mermaid
---
title: "Listing Service C4 Model: Component Diagram"
---

flowchart
    classDef container fill:#1168bd,stroke:#0b4884,color:#ffffff
    classDef externalSystem fill:#666,stroke:#0b4884,color:#ffffff
    classDef component fill:#855bbf0,stroke:#5d82a8,color:#000000
    
    Browser["Browser
    [Web Browser]
    
    Used by a user to browse
    the website"]
    
    MA["Application
    [Xamarin Application]
    
    Allows members to view and review
    titles from their mobile devices"]
    
    R["In-Memory Cache
    [Redis]
    
    Titles and their reviews
    are cached"]
    
    K["Message Broker
    [Kafka]
    
    Important domain events are published to Kafka"]
    
    TS["Title Service
    [Software System]
    
    Provides an API to retrieve
    title information
    "]
    
    RS["Review Service
    [Software System]
    
    Provides an API to retrieve
    and submit reviews"]
    
    SS["Search Service
    [Software System]
    
    Provides an API to search
    for titles"]
    
    TCont["Title Controller
    [ASP.NET MVC Controller]
    
    Allows users to view details
    about titles"]
    
    SCont["Search Controller
    [ASP.NET MVC Controller]
    
    Allows users to search for titles"]
    
    RCont["Review Controller
    [ASP.NET MVC Controller]
    
    Allows users to read and
    write reviews"]
    
    TComp["title Component
    [ASP.NET NAmespace]
    
    Provides information on titles,
    retrieves information from the title service
    and caches titles"]
    
    SComp["Search Component
    [ASP.NET Namespace]
    
    Searches titles using the
    search service"]
    
    RComp["REview Component
    [ASP.NET Namespace]
    
    Provides review information,
    submits new reviews
    and publishes domain events"]
    
    Browser--"Submits requests to\n[HTTPS]"--->TCont
    MA--"Submits requests to\n[HTTPS]"--->TCont
    
    MA--"Submits requests to\n[HTTPS]"--->SCont
    Browser--"Submits requests to\n[HTTPS]"--->SCont
    
    MA--"Submits requests to\n[HTTPS]"--->RCont
    Browser--"Submits requests to\n[HTTPS]"--->RCont
    
    
    subgraph listing-service[Listing Service]
        TCont--->TComp
        RCont--->TComp
        RCont--->RComp
        
        SCont--->SComp
    end
    
    TComp--->TS
    TComp--->R
    
    RComp--->R
    RComp--->K
    RComp--->RS
    
    SComp--->SS
    
    class MA,R container
    class SS,RS,TS,K,Browser externalSystem
    class RComp,SComp,TComp,RCont,SCont,TCont component
    style listing-service fill:none,stroke:#CCC,stroke-width:2px
    style listing-service color:#fff,stroke-dasharray:5 5
```

