# BIG DATA 
* It is the data whose size is huge. It consists of large datasets that can not be managed by common DBMSs,these datasets range from terabytes to exabytes.
 
* Big data originates from : sensors,online transaction,science and technology ,
  IOT devices,Health and education,Mobile phones
  Social media: - biggest source of generating data
                - 822 tweets/second,510 comments/minutes ,293000status updates 
                - 136000 photos are uploaded on Facebook
                - 11.5 million payments using paypal/day

# Evolution of Big Data
- In early 60s, technology witnessed real-time data problem so database came
- In 90s, problem with variety of data so noSQL came
- Now dealing with huge volume of data and big data came and evolving

# Characteristics of big data
4 Vs
1. Volume - quanity of dat
2. Variety - types of data
3. Velocity - rate at which data is generated,captured and processed
4. Veracity - accuracy and consistent data

# Realtime example
-  transportation- such as traffic jams for real time data(place,time and reasins)
-  education- online and distance learning
-  travel - booking, checking tickets
-  government - for preventive and corrective measure, weather forecasting
-  healthcare - to improve research and development practices, to store medical history of a patient
-  web-based business - big data helps to offer more appealing recommendations
-  sport - tracking tickets sales ,for tracking team strategies

# Types of data
Structured data + Semi-Structured data+ Unstructured Data = Big Data

1. Structured Data - It has defined repeating pattern or based on premitive data tuoes
It is easy to sort, read, process and analyze data. It is faster too
Sources : RDBMS,flat files(like excel), legacy database and multi dimwnsional database

2. Semi-structured data -  It is between structured and unstructured data
It contains tags or mark up elements to seperate elements and generate hierarchies of records and files
example : Table values seperate by comma
Sources : Web data in the form of cookies(XML)
          Data exchange format such as JSON

3. Unstructured data - It has no repeating pattern , 70-80% of data is unstructutred data
example : Metadata (data about data )
          Inconsistent data( from files )
          Different format(e-mails,text,audio,images etc)
sources : social media , mobile data, text both internal & external organization, log data

Challenges:
- Identifying the unstructured data
- sorting and organizing
- combining and linking
- costing(storage, analysts, scientists)

Pre requisites for big data analyst -
- Hadoop ecosystems components such as HDFs,MapReduce,Pig,Hive etc
- knowledge of NLP
- knowledge of maths and statistics
- knowledge of Machine Learning
- Data science

For big data developer : 
- programming skills Java, Python, Hadoop, Hive and Hbase
- HDFs and MapReduce
- knowledge of Zookeeper, Flume and Sqoop

# Why Big data analytics?
- Big data analytics helps to uncover information such as hidden patterns , unknown 
correlations, market trends and customer preferences that can help the organization informed business decisions
- It helps to collect accurate data , take timely informed strategic decisions and 
target the right side of audience and customers, increase the benefits , reduce wastage and costs

# Types of Big data analytics 
3 types
1. Descriptive analytics : It analyzes a database to provide info. on the trends of past or current business event that can help the managers , plan leaders etc to develop a road map for future
It discusses: 
- frequency of events 
- operations cost
- reason for failure
        
2. Predictive analytics :
What could happen ?
Understanding, predicting the future by using statistical models, different forcast techniques and machine learning etc

3. Prescriptive analytics :
What should we do ?
Based on the data obtained from descriptive and predictive analysis and by using the optimiztion techniques we should determine the finest substitute or solution for the problem

# HADOOP 

* Normal distributed file system:
In distributed file system both data and computation are distributed to a set of nodes .
Aim is to meet
(client sends request to server , server accepts or rejects and do the modification)
- scalability : Increasing no. of machines results in linear increase in processing capacity and storage
- Fault tolerance / resource : If one node fails the main computation should not fail 
- Recoverability/data : If a job or its part fails, data should not be lost

Drawbacks:
If data would be of huge size ,cost will increase
If Heterogenious data would be there it will be more complex to handle + expensive
If real time data or NoSQL data would be there , it will be difficult +very expensive  to deal 

* Hadoop 
Hadoop is an open source framework which is designed to process a large volume distributed data across the multiple computers(clusters) using simple programming model.
It is designed to scale up from a single server to thousands of machines each
each of them is offering local computation and storage 
cloud computing -> hadoop gains popularity

Features or Advantages of Hadoop:
- scalibility
- Fault tolerance
- Recoverability
- Large distributed system
- Fast processing 
- Streaming access
- Handling SQL and noSQL data
- Low cost 
- No movement of data

# Installing Hadoop

* JDK
Hadoop is written in Java therefore it is necessary to install Java Development Kit(JDK) which provides runtime environment(JRE) for its rograms and applications to run or execute

Commands(ctrl+alt+T)
1. $ sudo apt-get update 
2. $ sudo apt-get install openjdk-8-jdk 
          Or
    $ sudo apt=get install default-jdk
3. $ java -version

# Hadoop Architecture
 Hadoop has 2 main components:

 1. HDFS(Hadoop Distributed File System):
    Stores large volume of data over a network(cluster) of computers
    HDFS is designed for fast, fault-tolerant processing, thus enabling the use of inexpensive storage hardware
    MapReduce programming model is used to process and deal with large data volumes

Features of HDFS
- Handling large datasets
- Fault-tolerance
- Streaming access to data
- Simple data consistency

2. YARN(Yet Another Resource Negotiator):
 It is Hadoop processing layer, operating system , resource manager or scheduler
 YARN is designed to manage all resource in a Hadoop cluster
 YARN is a framework for managing distributed applications executed on multiple machines within a network
 It contains resource manager and job scheuler for both resources and jobs to handle 

# Hadoop Services
HDFS services(take care of the storage related work) and YARN services(set of computational services related to YARN)

1. HDFS services:
* Namenode : service runs on master node(main server) and maintains the metadat pertaining to HDFS storage:
- file system directory tree
- file's location
When client seeks to road or write to HDFS, it contacts the Namenode services, which provides the client information about the location of the file in HDFS.

* Secondary Namenode or Standby Namenode:
The services runs on master node amd relieves the burden of the critical Namenode by performing tasks such as updating the metadata file

* Datanodes:
This service runs on worker nodes that stores the HDFS data blocks on the linux file system. The Datanodes keep in contact with Namenode and update the latter with all the changes that occur in the fiile system.

2. YARN services:

* Resource manager : 
Runs on master node , allocating cluser's resource and scheduling jobs on the worker nodes

* Application manager : Runs on master node , coordinating the execution of applications in the cluster.

* Node manager : Runs on worker nodes , reports resource manager the health and task running.

# Pyhton 
- simple syntax
- easy to learn
- cross platform
- open source and free
- large standard libraries
- advance features

Commands to install
$ sudo apt-get update
$ sudo apt-get install python / python3
$ python --version
$python -V

# Hadoop 
3 modes of Hadoop installation 
* Standalone - only map reduce component will run
* Pseudo-distributed - single machine with 2JVMs 
* Fully-distributed - MapReduce, Yarn and HDFS run in this mode

* Video content 
Data from diff databses -> ETL  tools (eg informatica)-> data warehouse(OLAP) (We can use BI tools to visualize data)
ETL(Extract Transanct and load)
ETL tools drawbacks:
Limit work
Not real time data

MPP - Map parallel processing

# HADOOP
- MapReduce - Analyse data on top of Hadoop 
- Hadoop is an Open source framework with Apache / Cloudera, Hotworks, Mapr  lead company
- AWS offers fully managed hadoop solutions

* Distrubuted Computing
- One master , other slaves (storage purpose)/ We add more machine (scalabity) - - - CLUSTER
- It runs on cluster 

- ARCHITECTURE
HDFS (storage ), YARN(resource managing), MapReduce(processing)
Master (Namenode), slaves(Datanodes)
In HDFS modifying data is not possible. Only add or remove. 
Reads data sequencially 


Oozie in Hadoop -
Oozie is a tool which will help to schedule your program 
Process scheduling -> fair scheduler -> Queue (FIFO)

CLUSTER:
Webconsole(connect to linux)->cloudera manager (admin GUI )

In HDFS we use ELT 
- SQOOP is used to bring data from SQL /noSQL
- Apache Flume is point to point delivery tool .It is used to take data from a source gives to destinaiton. It is majorly used for unstructured data. 
- Flume can read the data and dump it to HDFS (It can store data anywhere) . It is pull based so it will not make any modification to the source that is why kafka is not used for this as one need to install kafka producer at the source which is not possible for the existing setup.
- So Kafka  runs on its own cluster (by default it can store data for 7 days or you can also customize it ) . 
- Spark streaming is utility/library which can do real time data processing. 
Flink and Storm are other examples of real time data analysing library


- MapReduce to process bunch files in HDFS/- MapReduce - Analyse data on top of Hadoop 
- Pig is a scripting tool in HDFS but not used much now a days
- Hive allows us to write SQL on the top of hadoop then it will convert it to MapReduce
- Spark is an in-memory execution engine . It is a batch processing system and it is very fast. 
- spark will communicate to hive to run SQL queries in hadoop

- Impala, hawq,llap,presto,drill - MPP(Map parallel processing) engines (For minute queries when we need not to load whole data)
It can run queries and scan the data by connecting to HDFS
MPP engines are less reliable then Hive that is why it is used for minute queries only

- HBase is the database of hadoop for noSQL/ realtime database.
It has an API and can do random read and data to HDFS . 
It gets install on HDFS and do random read and write but it has its own language/syntax.
- Phoenix(get all the metadata and runs SQL ) and HBase in combination works well

If we will take Hadoop from cloudera we will all this in one package but if we will download it from Apache we will get HDFS only

# MapReduce-
- It is not a language .
- It is a framework . 
- We can write MapReduce program in any language.  
- Uses divide and Conquer
- In MapReduce we write mapper program and reduce program
- Suppose ,we have Hadoop cluster and data nodes -> We have written mapper program which will work on each machine and Reduce will get the intermediate result and produce the final output.

(Example - Elections Delhi 
Process will go to the people instead of people going to the process
Mapper is phase1 of elections , Reducer will collect the result and final result will be given)

#If 100 mapper are there in code 10% of that will be reducer's count

It has very less dependencies 
* YARN will handle the execution like first mapper program execute and then Reducer

Example Wordcount to learn MapReduce
WORD COUNT  
Text file (big ) We stored it in 3 blocks of data 
Datanode1
Datanode2
Datanode3
We have to check the occurence of each word :
1. Develop Mapper
output should be in key, value pair

2. Mapper will run on each datanode
It will take every line one by one or record by record
Every word extracting will be key and value by default be 1

Output will be pushed to harddisk (if any datanode crashed so it has replica)

3. then shuffle and sort works(it will key and values)
4. after that reducer works( it will do the sum of values (we have to write logic in a program))

multiple reducer (if we have large amount of data it also do partitioning(hash ))
Data skewness (somewhere we have more data and somewhere less data)




