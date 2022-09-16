![spark](https://user-images.githubusercontent.com/105242871/190546620-008b665e-698e-4f3e-b986-b084e203d2c8.jpeg)


## Apache Spark Architecture
Spark is written in a language called scala, which runs on the Java Virtual Machine, or JVM. At first, in order to interact with spark, you had to write scala code, but now there are many different client libraries to interact with spark. This means you can harness spark's power using python, R, or a number of other langauges.

We will be using **pyspark**, the python interface to spark. Pyspark lets us write python code that manipulates spark dataframes (which, as we'll see, are similar to pandas dataframes), and the pyspark library will translate our python code into spark code that will run on the JVM.

Because pyspark is interfacing with spark, which is running on a JVM, we will sometimes see error messages and stack traces from Java when working with pyspark code.

***

## The Driver and Execution
Broadly speaking, a Spark application is broken into several areas:

1. The **Driver**: a single JVM (Java Virtual Machine) process, is responsible for analyzing your Spark program, optimizing your DataFrame queries, and determining how your Spark jobs should be parallelized.

2. The **Cluster Manager**: Gathers resources and schedules jobs on the cluster.

3. The **Executors**: which actually perform the distributed work.

Each Spark program has a single Driver, a Cluster Manager, and one or more Executors. The Driver is usually your laptop, which will be running pyspark and will be connected to a cluster.

[Spark API](spark-api.ipynb)

[Wrangle Class Demo](wrangle.ipynb)
***
# Exercises
[Spark 101](spark101.ipynb)

[Spark Wrangle](spark_wrangle.ipynb)
