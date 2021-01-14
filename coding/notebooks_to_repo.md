# Moving Notebooks to Repository Code

* Before starting: Make sure notebooks work properly
* Think of architecture:
     * What modules are needed
     * What is input and what is output of each component
     * How are modules connected
     * How do we avoid redundancy of functionality
     * Draw it
* Implement directory's structure: Store components as general as possible and as specific as necessary
* Implement functions file by file
     * For every function: 
          * Is it redundant, can we use another already implemented function?
          * Is a test needed, possible, worth it? 
          * Add typing of input and output
          * Add good documentation """ """
* Before making a change: 
     * Is this necessary to achieve acceptance criteria AND are there any tests AND are tests related to code to be refactored? Continue
          * Is this an improvement? Add TODO
               * Don't make that change today
* Small commits: One commit per functionality
* Collect commit into groups of 5(?) and run all tests locally before pushing
* Keep an eye on Jenkins CI, should always be green
* Small PRs: Group refactored files according to chosen orientation and create a PR for each group. RoT: One PR every (1-2) days.
* Deploy PRs step-by-step
