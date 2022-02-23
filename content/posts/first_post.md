---
title: "System Design Capstone"
date: 2022-02-23T00:33:37-08:00
description: "The project I learned from the most during HR."
type: post
tags: ["system design"]
---
## Part 1

SDC (System Design Capstone) was one of the most rewarding, yet challenging, applications I have had to work on.

Working with a team of 2 other engineers, our goal was to transform and breakdown a monolithic architecture into 3 different microservices. Our client had an e-commerce website with a legacy API, and needed us to revamp the backend to scale for production level web traffic. I was solely responsible for the user questions and answers widget, and was given millions of CSV files to load into the new database I had to design.

I knew I had to collect my thoughts and started off with debating between the pros and cons of different types of databases. The final two databases I ended up choosing between was MongoDB (Mongoose) and PostgresQL. The 'correct' choice would be based on the type of need.

### MongoDB/Mongoose
* Scales horizontally (scale-out)
* Works well with rapidly-changing, multi-structured data
* Better for agile in the beginning
* JSON/JS based
* Document-Oriented (fast reads)


### PostgresQL
* Scales vertically
* Relational data
* Data Integrity (ACID)
* Robust access-control system
* Fault-tolerant environments

Unfortunately the decision was not as clear-cut as I had hoped. I had the hardest time deliberating between the two.

