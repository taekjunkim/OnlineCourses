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
