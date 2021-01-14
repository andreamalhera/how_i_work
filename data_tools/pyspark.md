# Pyspark

## How to browse json files with pyspark
* make venv with python 3.7
* 'pip install ipython'
* 'pip install 'pyspark'
* 'ipython'
* 'import pyspark'
* 'sc= pyspark.SparkContext.getOrCreate()'
* 'spark = pyspark.sql.SparkSession(sc)'
* 'final_survey_reviews = spark.read.format('json').load('hdfs://<machine.domain.com>/<path/to/file>.jsonl')'
