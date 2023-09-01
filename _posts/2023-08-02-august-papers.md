---
layout: default
title: Paper Digest of August 2023
tags: [Database, Partitioning]
nav_order: {{ page.date }}
---


# Integrating Veritical and Horizontal Partitioning into Automated Physical Data Design

Author: Sanjay Agrawal, Vivek Narasayya, Beverly Yang  
Publisher: SIGMOD 2004  
This paper presents a new method to automatically recommend the physical database design. Unlike previous works which use a staged pradigm the new method combines the design space of vertical partitioning and horizontal partitioning. It presents a feasiable framework to generate data configurations out of huge combinations.


# Big Metadata: When Metadata is Big Data

Author: Pavan Edara, Mosha Pasumansky  
Publisher: PVLDB 2021  
Without a metadata system each query needs to open every block and check the block header for min-max values and bf before scan the data. This step is time consuming in queries. This paper presents a distributed metadata system used in Big Query. The metadata system concentrates the metadata for blocks and is stored in the same format as data. The paper also describes how to rewrite queries to use the metadata system. Aiding by the metadata information the new system can filter out many unqualified blocks. The experiment show the optimized system can improve query speed by up to 10x times.


# Towards a One Size Fits All Database Architecture

Author: Jens Dittrich, Alekh Jindal  
Publisher: CIDR 2011  
This paper presents OctopusDB. This Database does not has a fixed storage layout. OcotusDB invented a structured called storage views. All calls to the system are recorded as logs in the primary log store. By constructing different storage views to form a lattice it can emulates different types of systems (row stores, column stores, streaming stystems, and more).


# Birdging the Archipelago between Row-Stores and Column-Stores for Hybrid Workloads

Author: Joy Arulraj, Andrew Pavlo, Prashanth Menon  
Publisher: ICMD 2016  
This paper presents a HTAP system which can adapt to different worloads. OLTP workloads are in favor of row stores. And OLAP workloads are in favor of column stores. But HTAP workloads is mixture of these two workloads and even varies temporally and spatially. Instead of a fixed layout the system introduced by this paper decompose table data into physical tiles. These physical tiles can vary between a row-store and column-store based on database workloads. In order to decouple the query plan engine from the physical organization of physical tiles this system put logical tiles on top of physical tiles. These logical tiles contain row tuples. Instead of real data these logical tiles contain offsets to the positions of data in the physical tiles. In order to adapt the physical tiles to the workload this system uses KNN to find column clusters. And this algorithm can be run iteratively to track the workload change. The experiment shows that this system can adapt to workload change.


# GREP A Graph Learning Based Database Partitioning System

Author: Xuanhe Zhou, Guoliang Li, Jianhua Feng, Luyang Liu, Wei Guo  
Publisher: SIGMOD 2023  
This paper presents a horizontal partitioning method that works for distributed databases. The author uses graph to represent table relations and characterize join relations. The main contributions of this paper include an attention based graph vertex weight learning method to speed up learning process, an embedding method for vertex features and an evaluation model for partitioning schema rating.


# SageDB An Instance-Optimized Data Analytics System

Author: Jialin Ding, Ryan Marcus, Andreas Kipf, Tim Kraska, etc.  
Publisher: VLDB 2023  
Keywords: Instance-optimized Data Layout, Partial Materialized View  
This paper introduces a inteligent data analytics system named SageDB which uses two techiques to optimize for the given workload. One technique is called Partial Materialized View. The other is instance-optimized data layouts. This paper integrates these two technique into one system. A algorithm that interleaves the calculation of PMVs and data layouts until it converges is given. In the system a "OPTIMIZE" command is provided for the user to invoke the optimization process when the workload is changed.
