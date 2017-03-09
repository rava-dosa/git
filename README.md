# git
Cheatsheet

#Level 1

"Git commits"
>It can (when possible) compress a commit as a set of changes, or a "delta", from one version of the repository to the next.

"Git Branches"
>They are simply pointers to a specific commit -- nothing more
>git checkout -b [yourbranchname]

"Branches & merging"
>Now we need to learn some kind of way of combining the work from two different branches together. This will allow us to branch off, develop a new feature, and then combine it back in.
>git merge [branchname]

"Rebasing"
>The second way of combining work between branches is rebasing. Rebasing essentially takes a set of commits, "copies" them, and plops them down somewhere else.
>git rebase [branchnameto rebase]

"What is master"
>HEAD is the symbolic name for the currently checked out commit -- it's essentially what commit you're working on top of.HEAD always points to the most recent commit which is reflected in the working tree. Most git commands which make changes to the working tree will start by changing HEAD

>Detaching head means that initially head was pinting towards branch now it points towards commits

"Git References & Relative commits"
>Moving around in Git by specifying commit hashes can get a bit tedious. In the real world you won't have a nice commit tree visualization next to your terminal, so you'll have to use >git log to see hashes.
>The upside is that Git is smart about hashes. It only requires you to specify enough characters of the hash until it uniquely identifies the commit. So I can type fed2 instead of the long string above.
>Relative commits are powerful, but we will introduce two simple ones here:
Moving upwards one commit at a time with ^
Moving upwards a number of times with ~<num>

"Branch forcing"
>One of the most common ways I use relative refs is to move branches around. You can directly reassign a branch to a commit with the -f option. So something like:
git branch -f master HEAD~3

>git branch -f branch-name C"X"

"Reversing Changes"
>There are many ways to reverse changes in Git. And just like committing, reversing changes in Git has both a low-level component (staging individual files or chunks) and a high-level component (how the changes are actually reversed). Our application will focus on the latter.There are two primary ways to undo changes in Git -- one is using git reset and the other is using git revert. We will look at each of these in the next dialog

>git reset HEAD~1(git reset  branchname to which you have to reset checkd out branch.)

>git revert HEAD.It creates a new  commit like git merge.

"Cherry pick"
>editing  graph
>git cherry-pick C1 C2.....

"Interactive rebasing"
>All interactive rebase means is using the rebase command with the -i option.
>git rebase -i HEAD~4





