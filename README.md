# recommended-reading
A place to store articles etc that I feel contain important information.

# General Software Development 

These are general articles that I would encourage engineers working beside me to know about and to understand.
## Useful References
###SourceMaking 
https://sourcemaking.com/

An online reference covering several important books. It has a summary of Martin Fowler's Refactoring (Code Smells, Refactorings etc) and the Gang Of Four's Design Patterns. It also has a simple UML reference.

## Articles
### Nine Antipatterns  
http://sahandsaba.com/nine-anti-patterns-every-programmer-should-be-aware-of-with-examples.html

Covers a few important look-outs. This is not code anti-patterns per-se but more on the human side (eg Pre-Optimization).

### Intro to BDD - Dan North
http://dannorth.net/introducing-bdd/

This is an important article in my opinion - a lot of developers working with xUnit will tend to call their tests "testSomething." Starting your test names with "should" helps to direct people to focusing on the behavior.

### Post Mortems
I thought this was a really good read. Both the articles, and the comments.
Worth stewing with this for a bit.

Article: http://danluu.com/postmortem-lessons/

Comments: https://news.ycombinator.com/item?id=10090806

PostMortems: https://pinboard.in/u:peakscale/t:postmortem/

# Multicore Computing, Scaling Up

### 1024 Cores
http://www.1024cores.net/

This is an excellent blog to get you started. The general recipe is good to understand.

# Distributed Computing
### CAP Theorem
https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html

CAP is a very important concept to understand in distributed computing. It's also important to understand its limits. This article gives a good introduction to help you understand CAP.

### A comprehensive study of Convergent and Commutative
Replicated Data Types
http://hal.upmc.fr/inria-00555588/document

This paper discusses a principled type for using in eventually consistent systems. 

### Papers
http://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf

This paper describes the Amazon Dynamo DB and how it handles distributing data across nodes and gossiping changes to a cluster's topology. Cassandra would be an example of an datastore that is heavily influenced by the Dynamo paper.

### Aphyr Jepsen Series 
https://aphyr.com/tags/jepsen

These articles are tremendously useful for understanding how different technologies deal with (or moreso fail to deal with) network partitions. I would keep this close by if you're clustering most anything.

### Reactive Streams Presentation from Roland Khun
http://www.typesafe.com/resources/video/introducing-reactive-streams

This is a good overview of Reactive Streams and asynchronous non-blockind "back-pressure." Push based distributed systems can potentially overwhelm services, causing messages to be dropped or nodes could crash. Back-pressure allows us to pull messages as a service is able to handle the messages instead of overwhelming downstream systems. 

### WHAT WE TALK ABOUT WHEN WE TALK ABOUT DISTRIBUTED SYSTEMS
http://videlalvaro.github.io/2015/12/learning-about-distributed-systems.html

Overview of concepts.

### Distributed Locks
http://martin.kleppmann.com/2016/02/08/how-to-do-distributed-locking.html
Discussion about fencing, redlock etc. Thought it was a nice discussion of issues related to lock expiry.
Salvatore responded 
http://antirez.com/news/101

# Scala/Akka

### Don't Use Actors for Concurrency
https://www.chrisstucchio.com/blog/2013/actors_vs_futures.html

I do believe this is a good rule of thumb, but see also Extra and Cameo pattern as I don't always agree. Actors have other use cases where they improve design. I would say use actors for state and distribution. See the Extra and Cameo Pattern (below.)

### Extra and Cameo Pattern
http://www.slideshare.net/shinolajla/effective-akka-scalaio

I don't 100% agree with the "Don't use Actors for Concurrency." Jamie Allen writes about the Extra and Cameo patterns in his book "Effective Akka" - if you're collecting together data from multiple datasources, actors can be used to produce cleaner solutions without Ask/Futures - these patterns produce better solutions than futures alone and get rid of timeout stacktraces in your logs. These slides cover the patterns or grab a copy of the book. 

Note also that there is a great simplified actor dsl for temporary actors! http://doc.akka.io/docs/akka/snapshot/scala/actordsl.html

## Tools and Stuff
Scala-based load testing tool 
http://gatling.io/

# Courses
Self paced SICP: http://www.cs61as.org/index.html

# OPS
Timekeeping in VMs
http://www.vmware.com/files/pdf/Timekeeping-In-VirtualMachines.pdf

"My First 10 minutes on a server" - securing ubuntu
http://www.codelitt.com/blog/my-first-10-minutes-on-a-server-primer-for-securing-ubuntu/

# My Read List
has a bunch of references to look through/curate
http://the-paper-trail.org/blog/distributed-systems-theory-for-the-distributed-systems-engineer/
http://book.mixu.net/distsys/

