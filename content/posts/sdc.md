---
title: "System Design Capstone P.1"
date: 2022-02-23T00:33:37-08:00
description: "The project I learned from the most during HR."
series:
  - system-design
tags: ["system design"]
---

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

### The Decision

Unfortunately the decision was not as clear-cut as I had hoped. I had the hardest time deliberating between the two.

While designing the schemas for my database, I found clear relations between the users, questions, and answers. I had a hard time creating schemas with Mongoose, even when I tried to embed the documents. Mapping out the data into relational tables seemed more intuitive to me.

MongoDB/Mongoose initially seemed really appealing since I felt that it would allow me to quickly play with the schemas. It was more flexible than a relational database. Relational databases like mySQL and PostgresQL seemed a bit rigid, and I was also worried about scaling limitations.


I was also unfamiliar with PostgresQL, so I had to weigh whether or not learning new database syntax would be reasonable due to time constraints. However, I used mySQL before, and after a cursory read through the [documentation](https://www.postgresql.org/docs/current/), saw that there was some overlap between the two types of relational databases.

--- Part 2 in Progress ---