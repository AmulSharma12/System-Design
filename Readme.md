## 🚀 System Design

### What you learn ?

- Identiy basic design pattern to build large scale distribuited patterns.

## 🚀 Large scale distribuited system

### 🏹 Large Scale

- something being used a lot.
- e.g. google maps because
  - it has lot of data.
  - used by lot of people.
  - updated very frequently.
  - lot of performance expectation .

### 🏹 Distribuited system

- the server/code executing this program is not in one place.
- server distribuited around the world :-
- for Fault tolerance :-
  - if one of the server crashes rest of the server can take the load.
- for Performance :-
  - someone in india can talk to indian server for the quicker results.
  - if go in some overseas server they have to go accross continents- that wil make it slow.

## 🚀 Design Patterns

- To build the large scale distribuited system Enginnering teams depends on design patterns .
- Design patterns are some principles/practices/process to solve the problems.
- <b> Example</b>
  - <i>you have common problem - a celeb posting on social media that will go across to millions of people i.e. followers lets say it post on youtube and then on linkedin/instagram </i>
  - <b>If you look the problem is similar - one piece of content which has to be made into a event notified to millions of people </b>
  - <b>you have to notified them quickly also you dont want too much load into your service so the rest of the request coming into the server continuing to served. </b>
- Conclusion - you extract common problem and you extract common solution for it this would be a design pattern.
- For this problem the one kind of design pattern is <i> Publisher Subscriber model </i>.
  - where <i> Celeb</i> is publisher and their event subscibe to millions of people and intermediatory decide the pace at which notification send.
  - this will keep the server load low and also notification reach to the subscribers
- Now as as engineer, you can take business requirements, and convert them into the technical solution.
- Engineer used system design patterns to make reliable , scalable and maintainable systems.
- Don't worry if you dont know how to figure out the design pattern this is just a example of how the problems being solved and i also dont know before that but now its clear how to actually think/how they solve problems atleast using the example.

## 🚀 Live streaming system-design

- Let's say a company doing the broadcasting of vides to billions of people. e.g. hotstar, netflix, youtube etc.
- some sort of events broadcasting to millions of people you as a enginner have to come up with some solution that will solve this problem.

- <i> Step 1 </i>

  - Define the requirements from the user perspective.
  - Normally, this thing done by product manager not by engineer to write the Product requirement document based on:-
    - user-feedback and data.
  - Then, Engineer will come up to some solution.

- <i> Step 2 </i>

  1. Amongst them, you pick up the most important feature - able to watch the video live.
     - Being able to watch video live is the primary issue.
     - your server does not go down.
     - bandwidth requirements are sufficient.
  2. Reduce the features to data definitions
     - user should be able to like/comment on the video.
     - abstract concept of somebody liking something
     - means, particular user like particular comment.
     - I has likeid, userid, timestamp
     - comment itself as an abstract concept.

- Conclusion:-

  - Product requirement doc.
  - <b>taking feature/ abstract-concepts</b> convert them into :-
  - <b>data definitions</b> this than mapped into the :-
  - <b>Objects </b> then mapped into the
  - <b> Database</b>
  - once you define the data you need to store you need to define :-
  - <b> EndPoints </b> through which the data can be manipulated/queried.
  - give me the api through which we can get the data through the server

- While building a solution you have some engineering requirements.

## 🚀 Engineering requirements

### 🏹 Fault Tolerance

- none of your services fail in case of outage
  - <b><i>outage</i></b> - a period when services not available
- For example - your some service/comment-service failed in india and you dont want to collapse the system.
- Earlier, we talked about you have multiple server spread across the world to avoid single point of failure.
- Also you can have multiple servers in india itself.
  - Here you might have some sort of data duplication because of which other server quickly able to pick up the responsibility.
  - Or, you have some sort of partitioning that 50% of user going to this server and 50% going to another server- so just 50% of the user got effected.

### 🏹 Extensibility

- Its not just about technical solution you come up with but also how easy you can change if some of the new requirements came up. <i> means is it extensible ?</i>
- Conclusion :- Build a system that can scale and extends whenever the new requirements meet.

### 🏹 Testing

- The design is then tested by common/edge cases at high level.
- Can use some tools for e.g. :-

  - capactiy estimation - to test whether the design is feasible and making sense.

- <i> <b>NOTE : you have to test the design before get into the code </b> </i>

## 🚀 Sumarizing the requirements

- Streaming video
- Processing video
- Broadcasting - sending video to multiple customer
- Failproof - not failing.
- Advertisment - showing advertisment.
- Reactions - allowing reactions.
- Disclamers/news flashes
- Degradation of video quality - in case of low bandwidth.
- multiple device support.


