# Big-Data-Processing--Assignment

Compilation and execution of code-

Since these programs haven maven dependencies, the run configurations should be chosen accordingly as- clean build. 
-We have written these programs in NetBeans IDE which comes with in-built maven. 
-If you right-click on the project that you want to compile, you will find an option called "Clean and Build".
-After the compilation is complete, a jar file is created. THe path to that jar file can be followed from the output screen of the IDE.
-Copy this jar file to HUE interface.
-Copy the jar file from HUE iterface to your HDFS, using the command: hadoop fs -copyToLocal <jar's input path> <jar's output path>
-Run WordCount over .wet file-
(a)Fetch the WET files from S3 to HDFS, using command: hadoop distcp <Path to common crawl dataset's file> /tmp 
(b)Upload the jar on your master node from Hue.
(c)Run the jar file on your HDFS, using the command: hadoop jar <jar's local path> org.commoncrawl.examples.mapreduce.WETWordCount
-The results are in /tmp/cc.
