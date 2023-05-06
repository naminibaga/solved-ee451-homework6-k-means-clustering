Download Link: https://assignmentchef.com/product/solved-ee451-homework6-k-means-clustering
<br>
The objective of this assignment is to gain experience with programming using the MapReduce programming model [1] in Apache Spark Cluster programming framework [2]. Apache Spark supports SCALA, python and java as programming languages. This assignment uses python as the programming language. If you use any other language, please provide detailed instructions for running the program in your submission.

<h1>1             Installation</h1>

We will download the pre-built binaries of Apache Spark for Hadoop 2.7 or later. <strong>The steps for installation on Windows OS are as follows:</strong>

<ol>

 <li>Install python (https://www.python.org/downloads/). Make sure to check the option “Add python to PATH” while installing. (We have tested with python 3.6 and 3.8 but any similar version should work)</li>

</ol>

Figure 1: Spark Download link

<ol start="2">

 <li>Install Java 8 from (https://www.java.com/en/download/)</li>

 <li>Download Apache Spark 3.0.1 from the following website</li>

</ol>

(http://spark.apache.org/downloads.html). Make sure that the option package type is set to: “Pre-built for Hadoop 2.7”. See Figure 1.

<ol start="4">

 <li>You can extract the files from the downloaded tarball in any folder of your choice using the 7Zip tool.</li>

 <li>Open the extracted files and change directory to the root directory, namely, YOURPATH-</li>

</ol>

3.0.1-bin-hadoop2.7

<ol start="6">

 <li>Type: bin/spark-submit examples/src/main/python/pi.py. This command runs a spark application to calculate pi. If the program runs correctly, you are all set (It should print a line ”Pi is roughly xxx”).</li>

 <li>Note: You may need to install winutils and create another system environment variable to get rid of the error message ”ERROR Shell: Failed to locate the winutils binary in the hadoop binary path”. For more information on installing winutils, follow this easy-toread guide: https://deelesh.github.io/pyspark-windows.html#disqus_thread</li>

</ol>

<strong>The steps for installation on MAC OS are as follows:</strong>

<ol>

 <li>Install Python</li>

 <li>Install java 8: brew tap adoptopenjdk/openjdk brew cask install adoptopenjdk/openjdk/adoptopenjdk8</li>

 <li>Install Apache Spark: brew install apache-spark</li>

 <li>Open bash profile to add Spark path: vim ∼/.bash profile insert the following lines:</li>

</ol>

export SPARK HOME=/usr/local/Cellar/apache-spark/3.0.1/libexec export PYTHONPATH=$SPARK HOME/python/lib/py4j-0.10.9-src.zip:$PYTHONPATH

<ol start="5">

 <li>exit vim by esc, :wq and source ∼/.bash profile</li>

 <li>Same as step.6 for Windows: If you successfully see the output line for pi.py, you are all set.</li>

</ol>

<h1>2             K-means Clustering</h1>

Based on the discussion slides, complete the Map (mapToCluster) and Reduce (updatemeans) functions of ‘kmeans.py’ [50 points]. Run the program and submit the output file produced.[50 points]

The command lines for running the program on Windows/MAC OS can be found in the commandline.txt provided to you.