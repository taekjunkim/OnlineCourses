# Introduction to Big Data


## What launched the Big Data era?
Combination of a growing amount of data and on-demand (e.g., cloud) computing
* **on-demand computing**: computing anywhere and anytime


## What makes big data valuable?
Big data allows us to build better models, which produce higher precision results

Examples are ...
* **Recommendation Engines**: Personalized marketing data
* **Sentiment Analysis**
   * Natural language processing
* **Biomedical Application** 
   * Human genone sequencing 
   * Personalized treatment


## Characteristics of Big Data
The V's of Big Data
* **Volume**: scale of data
* **Velocity**: analysis of streaming data
   * different from **batch processing**
      * collect data --> clean data --> feed in chunks --> wait --> action
   * **real time processing**
      * instantly capture streaming data --> feed real time to machines --> process real time --> action
      * what's going on right now: data generated at a varied rates
* **Variety**: different forms of data
* **Veracity**: uncertainty of data = biases, noise, abnormality in data
   * Quality of data
   * Accuracy of data, Reliability of data source, Context within analysis
* **Valence**: connectedness


## Integrating Diverse Data
* Data Integration Process
   * Discovering, Accessing, Monitoring
   * Modeling, Transforming
* Data integration provides 
   * reduced data complexity, increased data availabilty, unify your data system
   * increase data collaboration
   * add value to your big data


## Getting value out of Big Data
* Data Science
   * Big Data --> Insight --> Action
   * keep updating the model for better prediction using historical data + near real-time data


## Steps in the Data Science Process
* Acquire Data: Identify suitable data, acquire all available data
   * Traditional databases: SQL and query brouwsers
   * Text files: Scripting languages
   * Remote data: Web Services
   * NoSQL storage: API + Web Services
* Prepare Data
   * Explore: understand nature of data (what it means, quality, and format), preliminary analysis
      * Correlations, General trends, Outliers
      * Summary statistics: mean, median, mode, rnage
      * Heat maps: where the hot stots are
      * Histogram: distribution of the data - skewness, unusual dispersion
      * Boxplots
      * Line graphs: how values change over time
      * Scatter plots: correlation between two variables
   * Pre-process: clean (e.g., filtering), transform - integrate (multiple data sources), package (to specific format)
      * Data Quality Issues: inconsistent values, duplicate records, missing values, invalid data, outliers
         * Remove data with missing values
         * merge duplicate records
         * generate best estimate for invalid values
         * remove outliers
      * Getting Data in Shape
         * Dimensionality reduction
         * Data manipulation (e.g., grouping)
         * Transformation
         * Feature selection: removing redundant features, combining features, creating new features
         * Scaling
* Analyze Data
   * Select analytical techniques, Build models
      * classification: to predict category of input data
      * regression: to predict numeric value
      * clustering: to organize similar items into groups
      * association analysis: to find rules to capture associations between items (e.g., diaper-beer connection)
      * graph analysis: to find connections between entitites
   * Modeling
      * select technique --> build model --> validate model
   * Model evaluation
      * Classification/Regression: predicted value vs. correct value
      * Clustering: if they make sense for your application
      * Association/Graph analysis: investigate what model predicts is actually happening
   * Sometimes, need to go back to previous step
* Communicate Results
   * decide what to present or repart as the biggest value
      * what is the punchline, what are the main results?
      * how do the result compared to the success criteria determined at the beginning of the project
   * How to present
      * scatter plots, line graphs, heat maps, etc
      * tables with details
* Apply Results: tunrning insights into action
   
   

## What is a Distributed File System?
* Long-term information storage
   * Access result of a process later
   * Store large amounts of information
   * Enable access of multiple process
* **Distributed File System (DFS)**
   * Data partitioning and Data replication
      * can provide: Data scalability, Fault tolerance, High concurrency


## Scalable Computing Over the Internet
* Commodity Cluster: affordable parallel computers with an average number of computing nodes
   * not as powerful as traditional parallel computers
   * often built out of less specialized nodes
   * distributed computing over the internet: reducing computing cost
* Architecture of a commodity cluster
   * computing nodes are clustered in racks, connected to each other via a fast network
   * computing in one or more of these clusters across a local area network (or the internet) is called distributed computing
   * enables data-parallelism
      * many jobs that share nothing can work on different data sets or parts of a data set
   * Fault-tolerance: resolve potentials for node-level system failures
      * redundant data storage
      * restart of failed individual parallel jobs


## Programming Models for Big Data
* Requirements for Big Data Programming Models
   * Support Big Data Operations
      * split volumes of data
      * access data fast
      * distribute computations to nodes
   * Handle Fault Tolerance
      * Replicate data partitions
      * Recover files when needed
   * Enable Adding More Racks
   * Optimized for specific data types
      * Document, Table, Key-Value, Graph, Multimedia, Stream


## Hadoop ecosystem
* Major goals
   * Enable Scalability to store large volumes of data on cheap commodity hardware
   * Handle Fault Tolerance: Be ready - crashes happen
      * ability to gracefully recover from problems
   * Optimized for a variety data types
      * text files, graph of social networks, streaming sensor data, raster images
   * Facilitate a Shared Environment
      * allow multiple jobs to execute simultaneously
   * Free to use, easy to find support


## Hadoop Distributed File System (HDFS)
* HDFS: foundation for Hadoop ecosystem. storage layer
   * Scalability to large data sets
      * up to 200 PB, 4500 servers, 1 billion files and blocks
   * Reliability to cope with hardware failures
* HDFS splits files across nodes for parallel access
   * default chunk size is 64 megabytes
   * Replication for fault tolerance: By default, HDFS maintains three copies of every block
* Customized reading to handle variety of file types. For example, 
   * Text files can be read "line by line" or "a word" at a time
   * Geospatial data can be read as vectors or rasters
* Two key components of HDFS:
   * NameNode for metadata: usually one per cluster
      * NameNode issues comments to DataNodes across the cluster
      * NameNode coordinates operations
      * Keeps track of file name, location in directory, etc
      * Mapping of contents on DataNode
   * DataNode for block storage: usually one per machine (each node in the cluster)
      * Listen to NameNode for block creation, deletion, replication (Fault tolerance, data locality)


## YARN: A Resource Manager for Hadoop
* Resource manage layer that sits just above the storage layer HDFS
* Interacts with applications and schedules resources for their use
   * providing a standard framework that customized application development in the Hadoop ecosystem
   * Giraph for graph data analysis, Storm for streaming data analysis, Spark for in-memory analysis
* Essential gears in YARN engine
   * Central Resource Manager = Ultimate decision maker 
      * controls all the resources, and decides who gets what
   * Each machine gets a Node Manager
      * Node manager operates at machine level and is in charge of a single machine
   * Application Master = personal negotiator
      * it negotiates resource from the resource manager
      * it talks to node manager to get its tasks completed
   * Container = a machine
      * abstract notions that signifies a resource that is a collection of CPU memory disk network and other resources within the computer


## MapReduce: Simple Programming for Big Results
* Programming model for the Hadoop ecosystem
* relies on YARN to schedule and execute parallel processing over the distributed file blocks in HDFS
* Several tools that use the MapReduce model to provide a higher level interface to other programming models
   * Hive: SQL like interface that adds capabilities that help with relational data modeling
   * Pig: high level data flow language that adds capabilities that help with process map modeling
* Traditional parallel programming requires experties on a number of computing and systems concepts
* MapReduce programming model greatly simplifies running code in parallel
   * Map: apply operation to all elements
      * Paralleization over the input
   * Shuffle and Sort
      * Parallelization grouping of data: individual key-value pairs
   * Reduce: summarize operation on elements
      * Parallelized to construct one output file
* MapReduce is bad for
   * Frequently changing data
   * Computations, that do have dependencies, cannot be expressed with MapReduce
   * Interactive analysis: MapReduce does not return any results until the entire process is finished


## When to Reconsider Hadoop?
* Use Hadoop
   * Future anticipated data growth
   * Long term availability of data
   * Want to use multiple applications over the same data store
   * High Volume, High Variety data
* Caution to use Hadoop
   * Small datasets
   * Advanced Algorithms that require a specific hardware type
   * Infrastructure replacement
   * Task level parallelism
   * Random Data Access


## Cloud Computing: An Important Big Data Enabler
* In-house hardward and software resource building
   * networking hardware, storage, processors, upgrades
   * hardware estimation is hard
   * software stacks are complex: latest, compatible, installation
* Cloud: IT infrastructure & applications on Rent over the Internet
   * Pay as you go
   * Quick implementation
   * deploying application on a server that is geographically closer to your client
   * resource estimation solved
   * work on your domain expertise
   * instantly get different resources: cpu, gpu, memory, disk


## Cloud Service Models: An exploration of choices
* IaaS: Get the hardware only
   * you: install and maintain OS, application software
* PaaS: Get the computing environment
   * you: application software 
* SaaS: Get full software on-demand
   * you: domain goals


## Values from Hadoop and Pre-built Hadoop Images
* e.g., Hortonworks, Cloudera
* provide step-by-step guides on how to set up pre-built images on the Cloud


## Copy your data into the Hadoop Distributed File System: work is done in a virtual machine (cloudera)
* Download a text file of words: words.txt
* Open a terminal shell
* Copy text file from local file sytem to HDFS
> hadoop fs -copyFromLocal words.txt
* check the text file was successfuly copied
> hadoop fs -ls
* Copy a file within HDFS
> hadoop fs -cp works.txt words2.txt
* Copy a file from HDFS to the local file system
> hadoop fs -copyToLocal words2.txt
* Delete a file in HDFS
> hadoop fs -rm words2.txt
