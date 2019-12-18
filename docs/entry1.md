
# Introduction

This is a pet project that scratches a few itches. After a very busy time in my life, I'm lucky enough to be enjoying a few months off. I spent November playing computer games. Now it's time for a bit of coding. 

Essentially, it's a message passing architecture that allows me to play with different languages and kubernetes settings. JSON events are passed into a system, enqueued, them consumed upstream, wrapped in envelopes and interred in a database.

The envelopes will identify which consumer persisted the event, for example 'Golang Consumer', 'Rust Consumer'. At the end of a run, I'll then be able to do a very primitive comparison about the IO throughput abilities of different languages. It is not meant as a benchmark, by any means, just some fun. 

Specific itches to scratch.

## 1. Learning Rust 

For various reasons, I've wanted to gain a handle on programming in Rust. I've approached it a few times over the years. Rust forms a keypoint in this application using a streaming JSON parser and the new async functionality.

The first service in the JSONator will be built in Rust. It will expose an endpoint that can absorb JSON events and enqueue them somehow. I've yet to identify the queue.

## 2. Learning Kubernetes  

The final system will be deployed onto kubernetes, so it's a chance for me to learn in this area. I've even had the idea of building a raspberry pi cluster to deploy the JSONator onto. We will see.

## 3. Polyglot Consumers

I like to experiment and learn different languages; usually superficially. I find it interesting to learn a wide range of languages before deciding upon one that interests me enough for a deep dive. This architecture will let me write consumers in a range of different languages going forward and learn their IO models.



## tldr
In mid 2016 I had to decided to take some time off between contracts. I wanted to skill up in Rust and Haskell. I was tired of programming with languages that didn't want to 