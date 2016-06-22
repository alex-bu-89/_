# Git workflow

This workflow is only a proposal and needs to be improve over time.
Any feedback is highly appreciated.

### Normal workflow

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
5. When your PR has been approved, you can squash all your commits

  * `git rebase -i HEAD~3 (3 being the number of commits you want to squash)`
  * `git push origin my_feature_branch` (if you did rebase before use `-f`)

6. Now, you can merge to master

  * `git push origin my_feature_branch:master `

### Workflow for staging and production

1. Choose some repository and click the "New pull request" button.
2. Select the base as `production` and the compare as `staging` (or `staging` and `master`, respectively).
3. Fill the title and the description fields.
4. All checks should have passed and after that click "Merge pull request" button.

<img alt="Ghost logo" src="https://googledrive.com/host/0B7tNkEBh3dIna3pCcVVsa2tPVlk/title.png" />
