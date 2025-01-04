# Databricks_Learning
Databrcks Learning Tutorial with commands

Data Reading:

a) Below is defalut function used in Databricks to get the info of file saved in Databricks catalog:

dbutils.fs.ls('/FileStore/tables/BigMart_Sales-1.csv')

Out[5]: [FileInfo(path='dbfs:/FileStore/tables/BigMart_Sales-1.csv', name='BigMart_Sales-1.csv', size=869537, modificationTime=1736005879000)]

b) Below command is used to read the data from CSV file/ Path -- and store the info in **df**

df = spark.read.format('csv').option('inferSchema',True).option('header',True).load('/FileStore/tables/BigMart_Sales-1.csv') 
### Above snippet read the csv fie and info stored in df -- dataframe  -- Transformatiom

2) Spark Jobs
Job 0 View(Stages: 1/1)
Job 1 View(Stages: 1/1)

df:pyspark.sql.dataframe.DataFrame = [Item_Identifier: string, Item_Weight: double ... 10 more fields]

c) Action/ trigger output command -- Lazy evalution

df.show()  ### Show the output not applicable format
df.display()  ### Output in tabular format
-------------------------------------------------------------






