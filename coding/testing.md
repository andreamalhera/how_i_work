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
   * Exporting necessary source variables `export SPARK_HOME=$PWD/$PATH/$TO/lib/python2.7/site-packages/pyspark`
      * Check which `$SPARK_HOME` you are using with `echo $SPARK_HOME`
      * Check which installed python version you are using with `which python`
* Testing repo: 
   * Pull and change to repo
   * Change to `master` branch: git `git checkout master`
   * Run tests `make test`
