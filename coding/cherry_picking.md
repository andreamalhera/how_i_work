# How to fix having commits in the wrong branch (cherry picking):

* Cherry-pick to right branch:
   * `git checkout <correct-branch>`
   * make sure you are in the correct branch `git branch`
   * `git cherry-pick <commit-to-be-moved>`
   * fix merge conflicts by hand if necessary: e.g. copy pasting the correct file from IDE
   * git push
* Reverting changes from wrong branch:
   * `git checkout <wrong-branch>`
   * make sure you are in the correct wrong branch `git branch`
   * `git revert <wrong commit>` For multiple commits, be sure to revert them in the correct reversed order.
   * fix merge conflicts by hand if necessary: e.g. copy pasting the correct file from IDE
   * git push
* Check if worked e.g. in IDE and if it did smile :slightly_smiling_face:

## References:
* https://ohshitgit.com/
