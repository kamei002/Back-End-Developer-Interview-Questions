Back-End Developer Interview Questions
======================================

This page has been translated to [Chinese](https://github.com/monklof/Back-End-Developer-Interview-Questions) by [monklof](https://github.com/monklof).

I started writing down this list as a personal reminder of topics I had the chance to discuss with colleagues and friends, and that I wanted to deepen...

I'm not a big fan of asking technical questions in job interviews: I rather prefer to sit together with candidates in front of some real code, hands on the keyboard, facing a real problem, and have a full day of pair programming, hopefully rotating with all the other team members. Yet, I feel some technical questions could be a good starting point to begin an engaging and nice conversation, and this can be useful to get a deeper knowledge of each others.

This repo collects a number of back end related questions that can be used when vetting potential candidates. It is by no means recommended to use every single question on the same candidate: that would take hours, and would have no sense at all, as they cover a too broad set of topics for a single developer's to possibly know. Browse the section you find more relevant for your context, and pick the questions that give you more ideas on the conversation to have.

### Notice
Most of the questions are open-ended, and some of them just don't have a *right* or a *wrong* answer. On the contrary, they are intended to be used as the starting point for a conversation that hopefully tells you more about the person's capabilities than a straight answer would. Personally, I would even choose the questions whose answers are not yet clear to me.

Again, I stress that just asking questions is hardly sufficient. Complete the interview with a long pair programming session with your candidates: it is one of the best opportunities to know each others' style and approach and to let candidates know some details about their future day job.

This project is admittedly inspired by [Front-end Job Interview Questions](https://github.com/darcyclarke/Front-end-Developer-Interview-Questions) by [@darcyclarke](https://github.com/darcyclarke)



### Where are the answers?

Sooner or later I will complete it with the relative answers. Feel free to contribute, it would be highly appreciated!


## <a name='toc'>Table of Contents</a>

  1. [Questions about Design Patterns](#patterns)
  1. [Questions about Code Design](#design)
  1. [Questions about languages](#languages)
  1. [Web Questions](#web)
  1. [Databases Questions](#databases)
  1. [NoSQL Questions](#nosql)
  1. [Code Versioning Questions](#codeversioning)
  1. [Concurrency Questions](#concurrency)
  1. [Questions about Distributed Systems](#distributed)
  1. [Questions about Software Lifecycle and Team Management](#management)
  1. [Questions about logic and algorithms](#algorithms)
  1. [Questions about Software Architecture](#architecture)
  1. [Questions about Service Oriented Architecture and Microservices](#soa)
  1. [Questions about Security](#security)
  1. [General Questions](#general)
  1. [Open Questions](#open)
  1. [Questions based on snippets of code](#snippets)
  1. [Bill Gates Style Questions](#billgates)



### [[↑]](#toc) <a name='patterns'>Questions about Design Patterns:</a>

1. Why are global and static objects evil? Can you show it with a code example?
1. Tell me about Inversion of Control and how it improves the design of code.
1. The Law of Demeter (the Principle of Least Knowledge) states that each unit should have only limited knowledge about other units and it should only talk to its immediate friends (sometimes stated as "don't talk to strangers"). Would you write code violating this principle, show why it is a bad design and then fix it?
1. Active-Record is the design pattern that promotes objects to include functions such as Insert, Update, and Delete, and properties that correspond to the columns in some underlying database table. In your opinion and experience, which are the limits and pitfalls of the this pattern?
1. Data-Mapper is a design pattern that promotes the use of a layer of Mappers that moves data between objects and a database while keeping them independent of each other and the mapper itself. On the contrary, in Active-Record objects directly incorporate operations for persisting themselves to a database, and properties corresponding to the underlying database tables. Do you have an opinion on those patterns? When would you use one instead of the other?
1. Why is it often said that the introduction of `null` is a "billion dollar mistake"? Would you discuss the techniques to avoid it, such as the Null Object Pattern introduced by the GOF book, or Option types?
1. Many state that, in Object-Oriented Programming, composition is often a better option than inheritance. What's you opinion?
1. What is an Anti-corruption Layer?
1. Singleton is a design pattern that restricts the instantiation of a class to one single object. Writing a Thread-Safe Singleton class is not so obvious. Would you try?
1. The ability to change implementation without affecting clients is called Data Abstraction. Produce an example violating this property, then fix it.
1. Write a snippet of code violating the Don't Repeat Yourself (DRY) principle. Then, fix it.
1. How would you deal with Dependency Hell?
1. Is goto evil? You may have heard of the famous paper "Go To Statement Considered Harmful" by Edsger Dijkstra, in which he criticized the use of the `goto` statement and advocated structured programming instead. The use of `goto` has always been controversial, so much that even Dijkstra's letter was criticized with articles such as "'GOTO Considered Harmful' Considered Harmful". What's your opinion on the use of `goto`?
1. The robustness principle is a general design guideline for software that recommends "*be conservative in what you send, be liberal in what you accept*". It is often reworded as "*be a tolerant reader and a careful writer*". Would you like to discuss the rationale of this principle?
1. Separation of Concerns is a design principle for separating a computer program into distinct areas, each one addressing a separate concern. There are a lot of different mechanisms for achieving Separation of Concerns (use of objects, functions, modules, or patterns such as MVC and the like). Would you discuss this topic?


### [[↑]](#toc) <a name='design'>Questions about Code Design:</a>

1. It is often said that one of the most important goals in Object-Oriented Design (and code design in general) is to have High Cohesion and Loose Coupling. What does it mean? Why is it that important and how is it achieved?
1. Why do array indexes start with '0' in most languages?
1. How do tests and TDD influence code design?
1. Write a snippet of code violating the Don't Repeat Yourself (DRY) principle. Then, explain why it is a bad design, and fix it.
1. What's the difference between cohesion and coupling?
1. What is refactoring useful for?
1. Are comments in code useful? Some say they should be avoided as much as possible, and hopefully made unnecessary. Do you agree?
1. What is the difference between design and architecture?
1. In TDD, why are tests written before code?
1. C++ supports multiple inheritance, and Java allows a class to implement multiple interfaces. What impact does using these facilities have on orthogonality? Is there a difference in impact between using multiple inheritance and multiple interfaces? Is there a difference between using delegation and using inheritance? [This question is from The Pragmatic Programmer, by Andrew Hunt and David Thomas]
1. What are the pros and cons of holding domain logic in Stored Procedures?
1. In your opinion, why has Object-Oriented Design dominated the market for so many years?
1. What would you do to understand if your code has a bad design?


### [[↑]](#toc) <a name='languages'>Questions about Languages:</a>

1. Tell me the 3 worst defects of your preferred language
1. Why is there a rising interest on Functional Programming?
1. What is a closure, and what is useful for? What's in common between closures and classes?
1. What are generics useful for?
1. What are higher-order functions? What are they useful for? Write one, in your preferred language.
1. Write a loop, then transform it into a recursive function, using only immutable structures (i.e. avoid using variables). Discuss.
1. What does it mean when a language treats functions as first-class citizens?
1. Show me an example where an anonymous function can be useful.
1. There are a lot of different type systems. Let's talk about static and dynamic type systems, and about strong and weak ones. You surely have an opinion and a preference about this topic. Would you like to share them, and discuss why and when would you promote one particular type system for developing an enterprise software?
1. What are namespaces useful for? Invent an alternative.
1. Talk about interoperability between Java and C# (in alternative, choose 2 other arbitrary languages)
1. Why do many software engineers not like Java?
1. What makes a good language good and a bad language bad?
1. Write two functions, one referentially transparent and the other one referentially opaque. Discuss.
1. What is a stack and what is a heap? What's a stack overflow?
1. Why is it important that in a language functions are first class citizens?
1. Some languages, especially the ones that promote a functional approach, allow a technique called pattern matching. Do you know it? How is pattern matching different from switch clauses?
1. Why do some languages have no exceptions by design? What are the pros and cons?
1. If `Cat` is an `Animal`, is `TakeCare<Cat>` a `TakeCare<Animal>`?
1. In Java, C# and many other languages, why are constructors not part of the interface?
1. In the last years there has been a lot of hype around Node.js. What's your opinion on using a language that was initially conceived to run in the browser in the backend?
1. Pretend you have a time machine and pretend that you have the opportunity to go to a particular point in time during Java's (or C#, Python, Go or whatever) history, and talk with some of the JDK architects. What would you try to convince them of? Removing checked exceptions? Adding unsigned primitives? Adding multiple-inheritance?



### [[↑]](#toc) <a name='web'>Questions about Web development:</a>
1. Why are first-party cookies and third-party cookies treated so differently?
1. How would you manage Web Services API versioning?
1. From a backend perspective, are there any disadvantages or drawbacks on the adoption of Single Page Applications?
1. Why do we usually put so much effort for having stateless services? What's so good in stateless code and why and when is statefulness bad?
1. REST and SOAP: when would you choose one, and when the other?
1. In web development, Model-View Controller and Model-View-View-Model approaches are very common, both in the backend and in the frontend. What are they, and why are they advisable?


### [[↑]](#toc) <a name='databases'>Questions about Databases:</a>

1. How would you migrate an application from a database to another, for example from MySQL to PostgreSQL? If you had to manage that project, which issues would you expect to face?
1. Why do databases treat null as a so special case? For example, why does ```SELECT * FROM table WHERE field = null``` not match records with null ``field`` in SQL?
1. ACID is an acronym that refers to Atomicity, Consistency, Isolation and Durability, 4 properties guaranteed by a database transaction in most database engines. What do you know about this topic? Would you like to elaborate?
1. How would you manage database schema migrations? That is, how would you automate changes to database schema, as the application evolves, version after version?
1. How is lazy loading achieved? When is it useful? What are its pitfalls?
1. The so called "N + 1 problem" is an issue that occurs when code needs to load the children of a parent-child relationship with a ORMs that have lazy-loading enabled, and that therefore issue a query for the parent record, and then one query for each child record. How to fix it?
1. How would you find the most expensive queries in an application?
1. In your opinion, is it always needed to use database normalization? When is it advisable to use denormalized databases?
1. Of of the Continuous Integration's techniques is called Blue-Green Deployment: it consists in having two production environments, as identical as possible, and in performing the deployment in one of them while the other one is still operating, and than in safely switching the traffic to the second one after some convenient testing. This technique becomes more complicated when the deployment includes changes to the database structure or content. I'd like to discuss this topic with you.


### [[↑]](#toc) <a name='nosql'>Questions about NoSQL:</a>

1. What is eventual consistency?
1. Brewer's Theorem, most commonly known as the CAP theorem, states that in the presence of a network partition (the P in CAP), a system's designer has to choose between consistency (the C in CAP) and availability (the A in CAP). Can you think about examples of CP, AP and CA systems?
1. How would you explain the recent rise in interest in NoSQL?
1. How does NoSQL tackle scalability challenges?
1. When would you use a document database like MongoDB instead of a relational database like MySQL or PostgreSQL?


### [[↑]](#toc) <a name='codeversioning'>Questions about code versioning:</a>

1. Why is branching with Mercurial or git easier than with SVN?
1. What are the pros and cons of distributed version control systems like Git over centralized ones like SVN?
1. Could you describe GitHub Flow and GitFlow workflows?
1. What's a rebase?
1. Why are merges easier with Mercurial and Git than with SVN and CVS?


### [[↑]](#toc) <a name='concurrency'>Questions about Concurrency:</a>

1. Why do we need concurrency, anyway? Explain.
1. Why is testing multithreaded/concurrent code so difficult?
1. What is a race condition? Code an example, using whatever language you like.
1. What is a deadlock? Would you be able to write some code that is affected by deadlocks?
1. What is process starvation? If you need, let's review its definition.
1. What is a wait free algorithm?


### [[↑]](#toc) <a name='distributed'>Questions about Distributed Systems:</a>

1. How would you test a distributed system?
1. When would you apply asynchronous communication between two systems?
1. What are the general pitfalls of remote procedure calls?
1. If you are building a distributed system for scalability and robustness, what are the different things you'd think of if you are working in a closed and secure network environment versus when you are working in a geographically distributed and public system?
1. How would you manage fault tolerance in a web application? What about in a desktop one?
1. How would you deal with failures in a distributed system?
1. Let's talk about the several approaches to reconciliation after network partitions.
1. What are the fallacies of distributed computing?
1. When would you use request/reply and when publish/subscribe?
1. Suppose the system you are working on does not support transactionality. How would you implement it from scratch?


### [[↑]](#toc) <a name='management'>Questions about Software Lifecycle and Team Management:</a>

1. What is agility?
1. How would you deal with legacy code?
1. Say I'm your project manager, and I'm no expert in programming. Would you try explaining to me what legacy code is and why should I care about code quality?
1. I'm the CEO of your company. Explain to me Kanban and convince me to invest in it.
1. What is the biggest difference between Agile and Waterfall?
1. Being a team manager, how would you deal with the problem of having too many meetings?
1. How would you manage a very late project?
1. "*Individuals and interactions over processes and tools*" and "*Customer collaboration over contract negotiation*" comprise half of the values of the Agile Manifesto. Discuss
1. Tell me what decisions would you take if you could be the CTO of your Company.
1. Are program managers useful?
1. Organize a development team using flexible schedules (that is, no imposed working hours) and "take as you need" vacation policy
1. How would you manage a very high turn over and convince developers not to leave the team, without increasing compensation? What could a company improve to make them stay?
1. What are the top 3 qualities you look for in colleagues, beyond their code?
1. What are the top 3 things you wish non-technical people knew about code?
1. Imagine your company gives you 1 month and some budget to improve your and your colleagues' daily life. What would you do?


### [[↑]](#toc) <a name='algorithms'>Questions about logic and algorithms:</a>

1. Make a FIFO queue using only LIFO stacks. Then build a LIFO stack using only FIFO queues.
1. Write a snippet of code affected by a stack overflow.
1. Write a tail-recursive version of the factorial function.
1. Using your preferred language, write a REPL that echoes your inputs. Evolve it to make it an RPN calculator.
1. How would you design a "defragger" utility?
1. Write a program that builds random mazes.
1. Write a sample program that produces a memory leak.
1. Generate a sequence of unique random numbers.
1. Write a simple garbage collection system.
1. Write a basic message broker, using whatever language you like.
1. Write a very basic web server. Draw a road map for features to be implemented in the future.
1. How would you sort a 10GB file? How would your approach change with a 10TB one?
1. How would you programmatically detect file duplicates?


### [[↑]](#toc) <a name='architecture'>Questions about Software Architecture:</a>

1. When is a cache not useful or even dangerous?
1. Why does Event-Driven Architecture improve scalability?
1. What makes code readable?
1. What is the difference between emergent design and evolutionary architecture?
1. Scale out vs scale up: how are they different? When to apply one, when the other?
1. How to deal with failover and user sessions?
1. What is CQRS (Command Query Responsibility Segregation)? How is it different from the oldest Command-Query Separation Principle?
1. The so called "multitier architecture" is an approach to design a client–server system aimed to keep physically and logically separated presentation, application processing, data management and other functions. The most widespread of the multitier architectures is the three-tier architecture. Would you discuss the pros and cons of such an approach?
1. How would you design a software system for scalability?
1. Someone gave the name "The "C10k problem" to the problem of optimising network sockets to handle over 10.000 open connections at once. While handling 10.000 concurrent clients is not the same as handling 10.000 open connection, the context is similar. It's a tough challenge anyway, and no one is expected to know every single detail to solve it. It may be interesting to discuss the strategies you know to deal with that problem. Would you like to try?
1. How would you design a decentralized (that is, with no central server) P2P system?
1. You may recall that Common Gateway Interface (CGI) is a standard protocol for web servers to execute programs (CGI scripts) that execute as Command-line programs on a server, and that dynamically generate HTML pages when invoked by a HTTP request. Perl and PHP used to be common languages for such scripts. In CGI, a HTTP request generally causes the invocation of a new process on the server, but FastCGI, SCGI and other approaches improved the mechanism, raising the performance, with techniques such as preforking processes. Can you discuss why CGI became obsolete, and was instead replaced with other architectural approaches?
1. How would you defend the design of your systems against vendor Lock-in?
1. What are the disadvantages of the publish-subscribe pattern at scale?
1. What's new in CPUs since the 80s, and how does it affect programming?
1. In which part of the lifecycle of a software performance should be taken in consideration, and how?
1. How could a denial of service arise not maliciously but due to a design or architectural problem?
1. What’s the relationship between performance and scalability?
1. When is it OK (if ever) to use tight coupling?
1. What characteristic should a system have to be cloud ready?
1. Does unity of design imply an aristocracy of architects? Putting it simple: can good design emerge from a collective effort of all developers?
1. What's the difference between design, architecture, functionality and aesthetic? Discuss.



### [[↑]](#toc) <a name='soa'>Questions about Service Oriented Architecture and Microservices:</a>
1. Why, in a SOA, long-lived transactions are discouraged and sagas are suggested instead?
1. What are the differences between SOA and microservice?
1. Let's talk about web services versioning, version compatibility and breaking changes.
1. What's the difference between a transaction and a compensation operation in a saga, in SOA?
1. When is a microservice too micro?
1. What are the pros and cons of microservice architecture?


### [[↑]](#toc) <a name='security'>Questions about Security:</a>
1. How do you write secure code? In your opinion, is it one of the developer's duties, or does it require a specialized role in the company? And why?
1. Why is it said that cryptography is not something you should try to invent or design yourself?
1. What is two factor authentication? How would you implement it in an existing web application?
1. If not carefully handled, there is always a risk of logs containing sensitive information, such as passwords. How would you deal with this?
1. Write down a snippet of code affected by SQL injection and fix it.
1. How would it be possible to detect SQL injection via static code analysis? I don't expect you to write an algorithm capable of doing this, as it is probably a huge topic, but let's discuss a general approach.
1. What do you know about Cross-Site Scripting? If you don't remember it, let's review online its definition and let's discuss about it.
1. What do you know about Cross-Site Forgery Attack? If you don't remember it, let's review online its definition and let's discuss about it.
1. How does HTTPS work?
1. What's a man-in-the-middle Attack, and why does HTTPS help protect against it?
1. How can you prevent the user's session from being stolen? Chances are you remember what session or cookie hijacking is, otherwise let's read its Wikipedia page together.


### [[↑]](#toc) <a name='general'>General Questions:</a>

1. Why does functional programming matter? When should a functional programming language be used?
1. How do companies like Microsoft, Google, Opera and Mozilla profit from their browsers?
1. Why does opening a TCP socket have a large overhead?
1. What is encapsulation important for?
1. What is a real-time system and how is it different from an ordinary system?
1. What's the relationship between real-time languages and heap memory allocation?
1. Immutability is the practice of setting values once, at the moment of their creation, and never changing them. How can immutability help write safer code?
1. What are the pros and cons of mutable and immutable values.
1. What's the Object-Relational impedance mismatch?
1. Which principles would you apply to define the size of a cache?
1. What's the difference between TCP and HTTP?
1. What are the tradeoffs of client-side rendering vs. server-side rendering?
1. How could you develop a reliable communication protocol based on a non-reliable one?
1. [Tony Hoare](https://en.m.wikipedia.org/wiki/Tony_Hoare) who invented the null reference once said "*I call it my billion-dollar mistake*" since it led to "*innumerable errors, vulnerabilities, and system crashes, which have probably caused a billion dollars of pain and damage in the last forty years*". Imagine you want to remove the possibility to have null references in your preferred language: how would you achieve this goal? What consequences could this have?


### [[↑]](#toc) <a name='open'>Open Questions:</a>
1. Why do people resist change?
1. Explain threads to your grandparents
1. As a software engineer you want both to innovate and to be predictable. How those two goals can coexist in the same strategy?
1. What makes good code good?
1. Explain streaming and how you would implement it.
1. Say your company gives you one week you can use to improve your and your colleagues' lifes: how would you use that week?
1. What did you learn this week?
1. There is an aesthetic element to all design. The question is, is this aesthetic element your friend or your enemy?
1. List the last 5 books you read.
1. How would you introduce Continuous Delivery in a successful, huge company for which the change from Waterfall to Continuous Delivery would be not trivial, because of the size and complexity of the business?
1. When does it make sense to reinvent the wheel?
1. Let's have a conversation about "*reinventing the wheel*", the "*not invented here syndrome*" and the "*eating your own food*" practice
1. What's the next thing you would automate in your current workflow?
1. Why is writing software difficult? What makes maintaining software hard?
1. Would you prefer working on green field or brown field projects? Why?
1. [What happens when you type google.com into your browser and press enter?](https://github.com/alex/what-happens-when)
1. What does an operating system do when it has got no custom code to run, and therefore it looks idle? I would like to start a discussions about interrupts, daemons, background services, polling, event handling and so on.
1. Explain Unicode and database transactions to a 5 year old child.
1. Defend the monolithic architecture.
1. What does it mean to be a "professional developer"?
1. Is developing software an art, a craftsmanship or an engineering endeavour? Your opinion.
1. "People who like this also like... ". How would you implement this feature in an e-commerce shop?
1. Why are corporations slower than startups in innovating?
1. What have you achieved recently that you are proud of?



### [[↑]](#toc) <a name='snippets'>Questions about snippets of code:</a>
1. What's the output of this Javascript function?
```javascript
function hookupevents() {
  for (var i = 0; i < 3; i++) {
    document.getElementById("button" + i)
      .addEventListener("click", function() {
        alert(i);
      });
  }
}
```

1. About Type Erasure, what's the output of this Java snippet, and why?
```java
ArrayList<Integer> li = new ArrayList<Integer>();
ArrayList<Float> lf = new ArrayList<Float>();
if (li.getClass() == lf.getClass()) // evaluates to true
  System.out.println("Equal");
```


1. Can you spot the memory leak?
```java
public class Stack {
    private Object[] elements;
    private int size = 0;
    private static final int DEFAULT_INITIAL_CAPACITY = 16;

    public Stack() {
        elements = new Object[DEFAULT_INITIAL_CAPACITY];
    }

    public void push(Object e) {
        ensureCapacity();
        elements[size++] = e;
    }

    public Object pop() {
        if (size == 0)
            throw new EmptyStackException();
        return elements[--size];
    }

    /**
     * Ensure space for at least one more element, roughly
     * doubling the capacity each time the array needs to grow.
     */
    private void ensureCapacity() {
        if (elements.length == size)
            elements = Arrays.copyOf(elements, 2 * size + 1);
    }
}
```

1. `if`s and in general conditional statements lead to procedural and imperative programming. Can you get rid of this `switch` and make this snippet more object oriented?

```java
public class Formatter {

    private Service service;

    public Formatter(Service service) {
        this.service = service;
    }

    public String doTheJob(String theInput) {
        String response = service.askForPermission();
        switch (response) {
        case "FAIL":
            return "error";
        case "OK":
            return String.format("%s%s", theInput, theInput);
        default:
            return null;
        }
    }
}
```


1. Can you get rid of these `if`s and make this snippet of code more object oriented?

```java
public class TheService {
    private final FileHandler fileHandler;
    private final FooRepository fooRepository;

    public TheService(FileHandler fileHandler, FooRepository fooRepository) {
        this.fileHandler = fileHandler;
        this.fooRepository = fooRepository;
    }

    public String Execute(final String file) {

        final String rewrittenUrl = fileHandler.getXmlFileFromFileName(file);
        final String executionId = fileHandler.getExecutionIdFromFileName(file);

        if (executionId.equals("") || rewrittenUrl.equals("")) {
            return "";
        }

        Foo knownFoo = fooRepository.getFooByXmlFileName(rewrittenUrl);

        if (knownFoo == null) {
            return "";
        }

        return knownFoo.DoThat(file);
    }
}
```

1. How would you refactor this code?

```js
function()
{
    HRESULT error = S_OK;

    if(SUCCEEDED(Operation1()))
    {
        if(SUCCEEDED(Operation2()))
        {
            if(SUCCEEDED(Operation3()))
            {
                if(SUCCEEDED(Operation4()))
                {
                }
                else
                {
                    error = OPERATION4FAILED;
                }
            }
            else
            {
                error = OPERATION3FAILED;
            }
        }
        else
        {
            error = OPERATION2FAILED;
        }
    }
    else
    {
        error = OPERATION1FAILED;
    }

    return error;
}
```

### [[↑]](#toc) <a name='billgates'>Bill Gates Style Questions:</a>
This section collects some weird questions along the lines of the [Manhole Cover Question](https://en.wikipedia.org/wiki/Microsoft_interview#Manhole_cover_question).

1. What would happen if you put a mirror in a scanner?
1. Imagine there's a perfect clone of yourself. Imagine that that clone is your boss. Would you like to work for him/her?
1. Interview me.
1. Why are Quora's answers better than Yahoo Answers' ones?
1. Let's play a game: defend Cobol against modern languages, and try to find as many reasonable arguments as you can.
1. Where will you be in 10 years?
1. You are my boss and I'm fired. Inform me.
1. I want to refactor a legacy system. You want to rewrite it from scratch. Argument. Then, switch our roles.
1. Your boss asks you to lie to the company. What's your reaction?
1. If you could travel back in time, which advice would you give to your younger self?
