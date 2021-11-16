# RDD-to-pandas-dataframe

First, let’s create an RDD by passing Python list object to sparkContext.parallelize() function. We would need this rdd object for all our examples below.

In PySpark, when you have data in a list meaning you have a collection of data in a PySpark driver memory when you create an RDD, this collection is going to be parallelized.

# Convert PySpark RDD to DataFrame

Converting PySpark RDD to DataFrame can be done using toDF(), createDataFrame(). In this section, I will explain these two methods.

# Using rdd.toDF() function

PySpark provides toDF() function in RDD which can be used to convert RDD into Dataframe

By default, toDF() function creates column names as “_1” and “_2”. This snippet yields below schema.

toDF() has another signature that takes arguments to define column names as shown below.


# Using PySpark createDataFrame() function

SparkSession class provides createDataFrame() method to create DataFrame and it takes rdd object as an argument.


# Using createDataFrame() with StructType schema

When you infer the schema, by default the datatype of the columns is derived from the data and set’s nullable to true for all columns. We can change this behavior by supplying schema using StructType – where we can specify a column name, data type and nullable for each field/column.


