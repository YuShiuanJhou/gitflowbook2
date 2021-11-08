# gitflowbook2
gitflowtest

branch
 - master
 - branch1

git checkout -b  branch1
git add . 
git commit -m "....."
git push --set-upstream origin branch1
.
.
.
.
(after several commits)

use rebase -i to combine branch1 commits (prepare for rebase to master)

git log --oneline
(find target commit to rebase)
git rebase -i {commit}
[edit by vim ]replace "pick" to "squash" to merge commit
[edit by vim] naming the last commit (first 1)
(will see Your branch and 'origin/branch1' have diverged,)
git push -f origin branch1
(start rebase to master)
git pull --rebase origin master
(modify conflic files)
git add {conflic files}
git rebase --continue
(add commit message)
