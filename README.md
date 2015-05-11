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

# Distributed Computing
### CAP Theorem
https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html

CAP is a very important concept to understand in distributed computing. It's also important to understand its limits. This article gives a good introduction to help you understand CAP.

### Amazon's Dynamo Paper
http://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf

This paper describes the Amazon Dynamo DB and how it handles distributing data across nodes and gossiping changes to a cluster's topology. Cassandra would be an example of an datastore that is heavily influenced by the Dynamo paper.

### Aphyr Jepsen Series 
https://aphyr.com/tags/jepsen

These articles are tremendously useful for understanding how different technologies deal with (or moreso fail to deal with) network partitions. I would keep this close by if you're clustering most anything.

# Scala/Akka

### Don't Use Actors for Concurrency
https://www.chrisstucchio.com/blog/2013/actors_vs_futures.html

I do believe this is a good rule of thumb, but see also Extra and Cameo pattern as I don't always agree. Actors have other use cases where they improve design. I would say use actors for state and distribution. See the Extra and Cameo Pattern (below.)

### Extra and Cameo Pattern
http://www.slideshare.net/shinolajla/effective-akka-scalaio

I don't 100% agree with the "Don't use Actors for Concurrency." Jamie Allen writes about the Extra and Cameo patterns in his book "Effective Akka" - if you're collecting together data from multiple datasources, actors can be used to produce cleaner solutions without Ask/Futures - these patterns produce better solutions than futures alone and get rid of timeout stacktraces in your logs. These slides cover the patterns or grab a copy of the book. 
