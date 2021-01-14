# How to Refactor

* Understand Input and Output (Look at the tests for this)
* Recognise refactoring potential:
    * e.g. different functionalities packed in one function
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
    * Smile :smile: (edited)
* How to search a file: `sudo find / -name <filename.extension>`
