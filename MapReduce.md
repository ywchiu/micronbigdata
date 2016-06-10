1. wget https://github.com/ywchiu/micronbigdata/raw/master/MapReduce/WordCount.java
2. export CLASSPATH=/usr/hdp/2.4.0.0-169/hadoop/hadoop-common.jar:/usr/hdp/2.4.0.0-169/hadoop/client/hadoop-mapreduce-client-core.jar
3. mkdir wordcount_classes
4. javac -d wordcount_classes WordCount.java
5. jar -cvf wordcount.jar -C wordcount_classes/ ./
6. yarn jar wordcount.jar org.myorg.WordCount /tmp/wc.txt /tmp/out