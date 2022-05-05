# Branch workflow

## Continue working while waiting on PR 

To avoid having to wait for a pull request to approved to continue working on a feature that depends on it, use the following workflow: 

* Create branch `A` based on the `main` branch and develop your code.
* Create pull request for `A`.
* Create branch `B` based on branch `A` and begin working on it.
* Once pull request for `A` has been approved, merge it to `main`.
* Commit all your changes on branch `B`.
* Update your local copy of main:
    * `git checkout main`
    * `git pull`
* Merge `main` into branch `B`:
    * `git checkout B`
    * `git merge main`
* Solve all merge conflicts. Usually it is OK to accept the newest version of the files (as you probably updated them in the changes you did from branch `A` to `B`). All the files in `main` that were changed or added since branch `B` was created will be merged as well (you can ignore those).
* Once you have merged `main` in to `B`, push it to the source:
    * `git push`
* Create pull request for branch `B`. 
* Repeat cycle as necessary.