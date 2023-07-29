---
layout: default
title: Paper Digest of July 2023
tags: [Database, Data Structures]
nav_order: {{ page.date }}
---


# Paper Digest of July 2023


## Monkey: Optimal Navigable Key-Value Store

Author: Niv Dayan, Manos Athanassoulis, Stratos Idreos. SIGMOD 2017
This paper presents Monkey. The paper gives the formal mode for the look-up, update and range query cost. The model is built on the merge policy, the write buffer size, and the false posstive rate for bloom filters. An algorithm is invented to find the optimal parameter setup for LSM-DB and given workload.


## SageDB: A Learned Database System

Author: Tim Kraska, etc. CIDR 2019
SageDB is a database system that uses leanred models, for example RMI based models, to optimize database system components. This paper expand the applications of learned models on database indices. It shows learned models can be used to estimate optimizer models, improve joins and sorting operations, task scheduling and mutliple dimensional indices.


## The Periodic Table of Data Structures

Author: Stratos Idreos, etc. IEEE Data Eng 2018
This paper presents the design space of Data Structures. The authors call it the Periodic Table of Data Structures. This paper distills the first principles of data structure design from design choices of data layouts. And this paper shows that by interpolating this design principles with current designs we can get new data structures. And with a technique called Learned Cost Model it is possible to infer the performance by only implementing a small part of the target data structures.
