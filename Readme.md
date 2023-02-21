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
