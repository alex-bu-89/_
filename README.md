# Git workflow

## Normal workflow

1. Create your branch and build your feature

  * `git checkout -b my_feature_branch`
  * ... make your changes
  * `git add . && git commit -m "My commit message"`
  * `git push origin my_feature_branch`

2. From time to time, get in sync with master

  * `git fetch --all`
  * `git rebase origin/master`

3. Keep working on your branch

  * ... make your changes ...
  * `git add . && git commit -m "My commit message"`
  * `git push origin my_feature_branch` (if you did rebase before use `-f`)

4. Create your PR on github.
5. Now, you can merge to master

  * `git push origin my_feature_branch:master `

## Workflow for staging and production

1. Choose some repository and click the "New pull request" button.
2. Select the base as `production` and the compare as `staging` (or `staging` and `master`, respectively).
3. Fill the title and the description fields.
4. All checks should have passed and after that click "Merge pull request" button.
