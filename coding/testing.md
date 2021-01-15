# Testing
## Program unit tests

## Program qa tests
* Evaluate what is your goal
* Evaluate if algorithm achieves the goal
* Note what is output and expected output of the test
* Code and test statement by statement
    * Make use of prints for this
* Whenever an error happens, understand the error first before acting on it.


## Running tests
* Build [make](https://www.gnu.org/software/make/manual/make.html) file in repo to run tests (e.g. using [pytest](https://docs.pytest.org/en/stable/#)) including
   * Installing dev requirements (e.g. `pip install -r requirements_dev.txt `), where as `requirements_dev.txt` includes dependencies in specific versions if necessary. (e.g. `pyspark==2.2.1`)
   * Exporting necessary source variables (e.g. `export SPARK_HOME=$PWD/$PATH/$TO/lib/python2.7/site-packages/pyspark`) in a `envvars.sh` which is `source envvars.sh` in `make test`
      * Check which `$SPARK_HOME` you are using with `echo $SPARK_HOME`
      * Check which installed python version you are using with `which python`
* For applications using utilities like below use e.g. [Docker](https://www.docker.com/): 
   * start docker: `docker-compose up`
   * start all utilities (e.g. hadoop and spark) in a `start-all.sh`
* Testing repo: 
   * Pull and change to repo
   * Change to `master` branch: git `git checkout master`
   * Run tests `make test`

## Tools
* [Apache Hadoop](https://hadoop.apache.org/) is a collection of open-source software utilities that facilitates using a network of many computers to solve problems involving massive amounts of data and computation. It provides a software framework for distributed storage and processing of big data using the MapReduce programming model.
* [Apache Spark](https://spark.apache.org/) Apache Spark is an open-source distributed general-purpose cluster-computing framework. Spark provides an interface for programming entire clusters with implicit data parallelism and fault tolerance.
* [More utilities](https://github.com/andreamalhera/how_i_work/tree/master/data_tools)
