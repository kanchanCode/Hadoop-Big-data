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


# Normal distributed file system:
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

# Hadoop 
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

# Why do we need Hadoop?

- The big tech giants like facebook, amazon, google, microsoft have built the infrastructure to store millions of servers(computers) in specific locations and provide them with all the high class needs according to the demands. These servers have specific locations where they can store data in hard drives and process them. Small or medium level companies can’t use them as they dont meet the expense of such infrastructure, however with cloud technologies, we all can get a number of servers with our requested hard drive space and everything customised just for us on a single click. 

- Hadoop does the managing of such tasks in those servers with the help of cloud technologies.

# Modules of Hadoop:
* HDFS: Hadoop Distributed File System. Google published its paper GFS and on the basis of that HDFS was developed. It states that the files will be broken into blocks and stored in nodes over the distributed architecture.
* Yarn: Yet another Resource Negotiator is used for job scheduling and managing the cluster.
* Map Reduce: This is a framework which helps Java programs to do the parallel computation on data using key value pairs. The Map task takes input data and converts it into a data set which can be computed in Key value pairs. The output of Map task is consumed by reduce task and then the output of reducer gives the desired result.
* Hadoop Common: These Java libraries are used to start Hadoop and are used by other Hadoop modules.

# Installing Hadoop

* JDK
Hadoop is written in Java therefore it is necessary to install Java Development Kit(JDK) which provides runtime environment(JRE) for its rograms and applications to run or execute

Commands(ctrl+alt+T)
1. $ sudo apt-get update 
2. $ sudo apt-get install openjdk-8-jdk 
          Or
    $ sudo apt=get install default-jdk
3. $ java -version

* su - username
* http://localhost:9870 to open hadoop gui

# Hadoop Architecture
 Hadoop has components:

 1. HDFS(Hadoop Distributed File System):
    Stores large volume of data over a network(cluster) of computers
    HDFS is designed for fast, fault-tolerant processing, thus enabling the use of inexpensive storage hardware
    MapReduce programming model is used to process and deal with large data volumes

Features of HDFS
- Handling large datasets
- Fault-tolerance
- Streaming access to data
- Simple data consistency

HDFS services(take care of the storage related work) and YARN services(set of computational services related to YARN)

HDFS services:
* Namenode : service runs on master node(main server) and maintains the metadat pertaining to HDFS storage:
- file system directory tree
- file's location
When client seeks to road or write to HDFS, it contacts the Namenode services, which provides the client information about the location of the file in HDFS.

* Secondary Namenode or Standby Namenode:
The services runs on master node amd relieves the burden of the critical Namenode by performing tasks such as updating the metadata file

* Datanodes:
This service runs on worker nodes that stores the HDFS data blocks on the linux file system. The Datanodes keep in contact with Namenode and update the latter with all the changes that occur in the fiile system.

* File Block In HDFS: Data in HDFS is always stored in terms of blocks. So the single block of data is divided into multiple blocks of size 128MB which is default and you can also change it manually. 

* Replication In HDFS Replication ensures the availability of the data. Replication is making a copy of something and the number of times you make a copy of that particular thing can be expressed as it’s Replication Factor. 
You can configure the Replication factor in your hdfs-site.xml file. 


2. YARN(Yet Another Resource Negotiator):
 It is Hadoop processing layer, operating system , resource manager or scheduler
 YARN is designed to manage all resource in a Hadoop cluster
 YARN is a framework for managing distributed applications executed on multiple machines within a network
 It contains resource manager and job scheuler for both resources and jobs to handle 
 
* Features of YARN 
- Multi-Tenancy
- Scalability
- Cluster-Utilization
- Compatibility 


 YARN services:

* Resource manager : 
Runs on master node , allocating cluser's resource and scheduling jobs on the worker nodes

* Application manager : Runs on master node , coordinating the execution of applications in the cluster.

* Node manager : Runs on worker nodes , reports resource manager the health and task running.
 
3. MapReduce:
- MapReduce is nothing but just like an Algorithm or a data structure that is based on the YARN framework. 
- The major feature of MapReduce is to perform the distributed processing in parallel in a Hadoop cluster which Makes Hadoop working so fast.
- first Map then Reduce works
- Input is provided to the Map() function then it’s output is used as an input to the Reduce

* If 100 mapper are there in code 10% of that will be reducer's count

- MapReduce to process bunch files in HDFS/- MapReduce - Analyse data on top of Hadoop 

- It is not a language .
- It is a framework . 
- We can write MapReduce program in any language.  
- Uses divide and Conquer
- In MapReduce we write mapper program and reduce program
- Suppose ,we have Hadoop cluster and data nodes -> We have written mapper program which will work on each machine and Reduce will get the intermediate result and produce the final output.

(Example - Elections Delhi 
Process will go to the people instead of people going to the process
Mapper is phase1 of elections , Reducer will collect the result and final result will be given)


Mapper will run on each datanode
It will take every line one by one or record by record
Every word extracting will be key and value by default be 1

Output will be pushed to harddisk (if any datanode crashed so it has replica)

Then shuffle and sort works(it will key and values)
After that reducer works( it will do the sum of values (we have to write logic in a program))

multiple reducer (if we have large amount of data it also do partitioning(hash ))
Data skewness (somewhere we have more data and somewhere less data)


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
- Hadoop works very much Fastest in this mode among all of these 3 modes.
-  Standalone Mode also means that we are installing Hadoop only in a single system.
- We mainly use Hadoop in this Mode for the Purpose of Learning, testing, and debugging.
- When your Hadoop works in this mode there is no need to configure the files – hdfs-site.xml, mapred-site.xml, core-site.xml for Hadoop environment. In this Mode, all of your Processes will run on a single JVM(Java Virtual Machine) and this mode can only be used for small development purposes.

* Pseudo-distributed - single machine with 2JVMs 
- All the daemons that are Namenode, Datanode, Secondary Name node, Resource Manager, Node Manager, etc. will be running as a separate process on separate JVM(Java Virtual Machine) or we can say run on different java processes that is why it is called a Pseudo-distributed.
- One thing we should remember that as we are using only the single node set up so all the Master and Slave processes are handled by the single system. Namenode and Resource Manager are used as Master and Datanode and Node Manager is used as a slave. A secondary name node is also used as a Master. The purpose of the Secondary Name node is to just keep the hourly based backup of the Name node.
- Hadoop is used for development and for debugging purposes both.
Our HDFS(Hadoop Distributed File System ) is utilized for managing the Input and Output processes.
We need to change the configuration files mapred-site.xml, core-site.xml, hdfs-site.xml for setting up the environment.

* Fully-distributed - MapReduce, Yarn and HDFS run in this mode
- This is the most important one in which multiple nodes are used few of them run the Master Daemon’s that are Namenode and Resource Manager and the rest of them run the Slave Daemon’s that are DataNode and Node Manager.

# Hadoop Configurations

HADOOP CONFIGURATION PROPERTIES:
There are 6 files that need to be changed while installing hadoop. These files are the hadoop configuration properties. They all have different tasks.
1. Hadoop-env.sh: this file is mostly configured as it consists of the environment variables and the path of jdk that the hadoop will be using. It needs to be configured first.The hadoop-env.sh file serves as a master file to configure YARN, HDFS, MapReduce, and Hadoop-related project settings.

#Hadoop Related Options bash.rc
export HADOOP_HOME=/home/hdoop/hadoop-3.2.1
export HADOOP_INSTALL=$HADOOP_HOME
export HADOOP_MAPRED_HOME=$HADOOP_HOME
export HADOOP_COMMON_HOME=$HADOOP_HOME
export HADOOP_HDFS_HOME=$HADOOP_HOME
export YARN_HOME=$HADOOP_HOME
export HADOOP_COMMON_LIB_NATIVE_DIR=$HADOOP_HOME/lib/native
export PATH=$PATH:$HADOOP_HOME/sbin:$HADOOP_HOME/bin
export HADOOP_OPTS="-Djava.library.path=$HADOOP_HOME/lib/native"

2. Core-site.xml: The core-site.xml file defines HDFS and Hadoop core properties.To set up Hadoop in a pseudo-distributed mode, you need to specify the URL for your NameNode, and the temporary directory Hadoop uses for the map and reduce process. Here the port numbers are also declared. 

<configuration>
<property>
<name>hadoop.tmp.dir</name>
<value>/home/hdoop/tmpdata</value>
</property>
<property>
<name>fs.default.name</name>
<value>hdfs://127.0.0.1:9000</value>
</property>
</configuration>

3. Hdfs-site.xml: The properties in the hdfs-site.xml file govern the location for storing node metadata, fsimage file, and edit log file. Configure the file by defining the NameNode and DataNode storage directories.Additionally, the default dfs.replication value of 3 needs to be changed to 1 to match the single node setup.We can even add properties of each block as the way it will get uploaded with blocksize property tag.

<configuration>
<property>
<name>dfs.data.dir</name>
<value>/home/hdoop/dfsdata/namenode</value>
</property>
<property>
<name>dfs.data.dir</name>
<value>/home/hdoop/dfsdata/datanode</value>
</property>
<property>
<name>dfs.replication</name>
<value>1</value>
</property>
</configuration>

4. Yarn-site.xml:  The yarn-site.xml file is used to define settings relevant to YARN. It contains configurations for the Node Manager, Resource Manager, Containers, and Application Master.

sudo nano $HADOOP_HOME/etc/hadoop/core-site.xml

<configuration>
<property>
<name>mapreduce.framework.name</name>
<value>yarn</value>
</property>
</configuration>

mapreduce 
sudo nano $HADOOP_HOME/etc/hadoop/mapred-site.xml

<configuration>
<property>
<name>mapreduce.framework.name</name>
<value>yarn</value>
</property>
</configuration>

sudo nano $HADOOP_HOME/etc/hadoop/yarn-site.xml

<configuration>
<property>
<name>yarn.nodemanager.aux-services</name>
<value>mapreduce_shuffle</value>
</property>
<property>
<name>yarn.nodemanager.aux-services.mapreduce.shuffle.class</name>
<value>org.apache.hadoop.mapred.ShuffleHandler</value>
</property>
<property>
<name>yarn.resourcemanager.hostname</name>
<value>127.0.0.1</value>
</property>
<property>
<name>yarn.acl.enable</name>
<value>0</value>
</property>
<property>
<name>yarn.nodemanager.env-whitelist</name>   
<value>JAVA_HOME,HADOOP_COMMON_HOME,HADOOP_HDFS_HOME,HADOOP_CONF_DIR,CLASSPATH_PERPEND_DISTCACHE,HADOOP_YARN_HOME,HADOOP_MAPRED_HOME</value>
</property>
</configuration>

To start hadoop cluster
./start-dfs.sh
./start-yarn.sh

To check daemons
jps

# SCHEDULE JOB USING YARN:
In Hadoop, we can receive multiple jobs from different clients to perform. The Map-Reduce framework is used to perform multiple tasks in parallel in a typical Hadoop cluster to process large size datasets at a fast rate. This Map-Reduce Framework is responsible for scheduling and monitoring the tasks given by different clients in a Hadoop cluster. But this method of scheduling jobs is used prior to Hadoop 2. 
Now in Hadoop 2, we have YARN (Yet Another Resource Negotiator). In YARN we have separate Daemons for performing Job scheduling, Monitoring, and Resource Management as Application Master, Node Manager, and Resource Manager respectively.
Mainly there are two types of map reduce tools for managing jobs,
Jobtracker : this comes with all the 3 schedulers with FIFO being the default.
Resource manager: this comes with capacity scheduler as default and FAIR scheduler.
 
 There are mainly 3 types of Schedulers in Hadoop:  
1. FIFO (First In First Out) Scheduler.
2. Capacity Scheduler.
3. Fair Scheduler.
These Schedulers are actually a kind of algorithm that we use to schedule tasks in a Hadoop cluster when we receive requests from different-different clients. 
A Job queue is nothing but the collection of various tasks that we have received from our various clients. The tasks are available in the queue and we need to schedule this task on the basis of our requirements. 

1. FIFO Scheduler
As the name suggests FIFO i.e. First In First Out, so the tasks or application that comes first will be served first. This is the default Scheduler we use in Hadoop. The tasks are placed in a queue and the tasks are performed in their submission order. In this method, once the job is scheduled, no intervention is allowed. So sometimes the high-priority process has to wait for a long time since the priority of the task does not matter in this method. 
Advantage: 
No need for configuration
First Come First Serve
simple to execute
Disadvantage: 
 
Priority of task doesn’t matter, so high priority jobs need to wait
Not suitable for shared cluster
 

. Capacity Scheduler
In Capacity Scheduler we have multiple job queues for scheduling our tasks. The Capacity Scheduler allows multiple occupants to share a large size Hadoop cluster. In the Capacity Scheduler corresponding to each job queue, we provide some slots or cluster resources for performing job operations. Each job queue has its own slots to perform its task. In case we have tasks to perform in only one queue then the tasks of that queue can access the slots of other queues also as they are free to use, and when the new task enters to some other queue then jobs running in its own slots of the cluster are replaced with its own job. 
Capacity Scheduler also provides a level of abstraction to know which occupant is utilizing the more cluster resource or slots, so that the single user or application doesn’t take inappropriate or unnecessary slots in the cluster. The capacity Scheduler mainly contains 3 types of the queue that are root, parent, and leaf which are used to represent cluster, organization, or any subgroup, application submission respectively. 
Advantage: 
Best for working with Multiple clients or priority jobs in a Hadoop cluster
Maximizes throughput in the Hadoop cluster
Disadvantage:  
More complex
Not easy to configure for everyone

3. Fair Scheduler
The Fair Scheduler is very much similar to that of the capacity scheduler. The priority of the job is kept in consideration. With the help of Fair Scheduler, the YARN applications can share the resources in the large Hadoop Cluster and these resources are maintained dynamically so there is no need for prior capacity. The resources are distributed in such a manner that all applications within a cluster get an equal amount of time. Fair Scheduler takes Scheduling decisions on the basis of memory, we can configure it to work with CPU also. 
As we told you it is similar to Capacity Scheduler but the major thing to notice is that in Fair Scheduler whenever any high priority job arises in the same queue, the task is processed in parallel by replacing some portion from the already dedicated slots. 
Advantages: 
Resources assigned to each application depend upon its priority.
it can limit the concurrent running task in a particular pool or queue.
Disadvantages: The configuration is required.  
 
 # WORDCOUNT
1. Step 1: Create a file with the name input.txt  and add some data to it.
 
2. Step 2: Create a mapper.py file that implements the mapper logic. It will read the data from STDIN and will split the lines into words, and will generate an output of each word with its individual count. 

#!/usr/bin/python3

# import sys because we need to read and write data to STDIN and STDOUT
import sys

# reading entire line from STDIN (standard input)
for line in sys.stdin:
	# to remove leading and trailing whitespace
	line = line.strip()
	# split the line into words
	words = line.split()
	
	# we are looping over the words array and printing the word
	# with the count of 1 to the STDOUT
	for word in words:
		# write the results to STDOUT (standard output);
		# what we output here will be the input for the
		# Reduce step, i.e. the input for reducer.py
		print '%s\t%s' % (word, 1)

3. cat <text_data_file> | python <mapper_code_python_file>

4. Create a reducer.py file that implements the reducer logic. It will read the output of mapper.py from STDIN(standard input) and will aggregate the occurrence of each word and will write the final output to STDOUT. 

#!/usr/bin/python3

from operator import itemgetter
import sys

current_word = None
current_count = 0
word = None

# read the entire line from STDIN
for line in sys.stdin:
	# remove leading and trailing whitespace
	line = line.strip()
	# splitting the data on the basis of tab we have provided in mapper.py
	word, count = line.split('\t', 1)
	# convert count (currently a string) to int
	try:
		count = int(count)
	except ValueError:
		# count was not a number, so silently
		# ignore/discard this line
		continue

	# this IF-switch only works because Hadoop sorts map output
	# by key (here: word) before it is passed to the reducer
	if current_word == word:
		current_count += count
	else:
		if current_word:
			# write result to STDOUT
			print '%s\t%s' % (current_word, current_count)
		current_count = count
		current_word = word

# do not forget to output the last word if needed!
if current_word == word:
	print '%s\t%s' % (current_word, current_count)

5. cat word_count_data.txt | python mapper.py | sort -k1,1 | python reducer.py

Now let’s start all our Hadoop daemons with the below command.

6. start-dfs.sh
7. start-yarn.sh
8. hdfs dfs -mkdir /word_count_in_python


syntax to copy a file from your local file system to the HDFS is given below:

9. hdfs dfs -copyFromLocal /path 1 /path 2 .... /path n /destination

10. hdfs dfs -ls /       # list down content of the root directory

11. hdfs dfs -ls /word_count_in_python    # list down content of /word_count_in_python directory

Let’s give executable permission to our mapper.py and reducer.py with the help of below command.
cd folder_name

12. chmod 777 mapper.py reducer.py     # changing the permission

Now let’s run our python files with the help of the Hadoop streaming utility as shown below.

13. hadoop jar /home/dikshant/Documents/hadoop-streaming-2.7.3.jar \

> -input /word_count_in_python/word_count_data.txt \

> -output /word_count_in_python/output \

> -mapper /home/dikshant/Documents/mapper.py \

> -reducer /home/dikshant/Documents/reducer.py

14. hdfs dfs -cat /word_count_in_python/output/part-00000
