# How to Refactor

* Before starting: Step out to the big picture: Think on how to tackle that specific refactoring: 
    * File oriented; error type oriented or sth. else? =: Orientation
* Before making a change: 
    * Is this necessary to achieve acceptance criteria AND are there any tests AND are tests related to code to be refactored? Continue
          * Is this an improvement? Add TODO
               * Don't 
* Related tests should be passing
* (Locally) Break related tests to make sure tests verify behaviour of code to be refactored
* Understand Input and Output (Look at the tests for this)
* Recognise refactoring potential:
   * e.g. different functionalities packed in one function
* Refactor and get related tests to pass
   * Small commits: One commit per change
   * When moving functionality to new function:
       * Write unit test first, so it forces you to think what is output and goal
       * Copy lines for new function from old one.
       * Consider parameters.
       * Make call from old function at first to not overcomplicate.
       * Make unit test pass
       * Reconsider best location for new function
       * Adapt or make new integration tests
       * Adapt calls
       * Drop lines that are not needed anymore in old function
       * Make integration tests pass
   * Collect commit into groups of 5(?) and run all tests locally before pushing
   * Keep an eye on Jenkins CI, should always be green
   * Small PRs: Group refactored files according to chosen orientation and create a PR for each group. RoT: One PR every (1-2) days.
   * Deploy PRs step-by-step
   * Smile :smile: (edited)

* How to search a file: `sudo find / -name <filename.extension>`
