# Software Deployment

## Deployment on staging or production
* For production:
  * Make sure deployed first in staging
  * Check last tag locally with `git tag`
  * Make new tag following: https://semver.org/
     * Make sure to be in the commit to be tagged 
     * `git tag $TAG_NAME`
     * `git push origin $TAG_NAME`
* Merge request from (master/stable) to (stable/production):
     * Use an informative title e.g. [Informative: Promoting master to stable]
     * Start [Jenkins](https://www.jenkins.io/) build. Even better: Set labels to trigger [Jenkins](https://www.jenkins.io/) builds.
* Log into excecuting machine `ssh $USERNAME@$MACHINE.$DOMAIN`
* start screen `screen`
* Log into excecuting user `sudo -iu $USER`
* cd repo
* pull repo
* Follow READ.ME 
     * For dependencies changes, rebuild dependencies. (e.g. make venv)
     * Activate venv
     * Run tests `python $RUN_FILE --env $ENV --use-test True`
* `crontab -e` to see how often code is executed 

## Application as a package
* checkout [pip install](https://pip.pypa.io/en/stable/reference/pip_install/) `pip install git+ssh://git@$LOCATION`

## Tools
* [Jenkins](https://www.jenkins.io/): Open source automation server
* [crontab](https://linux.die.net/man/5/crontab): daemon of the general form: "run this command at this time on this date".
  * `crontab -e` to see how often code is executed
* [pip install](https://pip.pypa.io/en/stable/reference/pip_install/): Install packages from Pypi, VCS urls, local project directories and, local or remote source archives. pip also supports installing from “requirements files”, which provide an easy way to specify a whole environment to be installed.
