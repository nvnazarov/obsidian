#SCM

[[GitHub]]
- [Git - Reference (git-scm.com)](https://git-scm.com/docs)
- [Git - Book (git-scm.com)](https://git-scm.com/book/en/v2)
## Useful Commands

1. Config:

2. Create git repository:

3. Stage / restore changes:

4. Commit staged changes:

5. History:

`git log`

6. Aliases:

7. Getting old versions:

8. Tagging:

`git tag` - see all tags
`git tag <tag>` - tag current version as `<tag>`
`git tag -d <tag>` - delete tag

9. Undoing changes not staged for committing:

`git checkout <file>` - return the committed version of a `<file>`

10. Undoing staged changes:

`git reset HEAD <file>` - remove `<file>` from stage
`git checkout <file>` - return the committed version of a `<file>`

11. Undoing committed changes:

`git revert HEAD` - create a reverting commit
`git revert <hash>`

12. Remove recent commits from a branch:

`git reset --hard <hash|tag>`
can also remove tag if it exists

13. Amending commit:

`git commit --amend -m "Add an author/email comment"`

14. Moving files

`git mv <file> <dir>` - moves file and stages it for commit

or

`mv <file> <dir>`
`git add <dir>/<file>`
`git rm <file>`

15. Create branch

`git checkout -b <name>`

or

`git branch <branchname>`
`git checkout <branchname>`

16. View all branches

`git log --graph --all`

17. Merge branches
`
`git checkout feature` - move to `feature` branch
`git merge main` - merge `main` into `feature`

conflicts

18. Rebase

`git checkout feature`
`git rebase main`

19. Cloning repository

`git clone <repositoryname> <newrepositoryname>`

20. Remote repositories

`git remote` - see all known remote repositories
`git remote show <remotename>` - see info about a remote repository

`git branch` - see all local branches
`git branch -a` - see all branches, including remote

`git fetch` - fetches new commits from remote repository, but not merging them into the local branches

We can manually merge branches (`git merge origin/main`)

`git pull` = `git fetch` + `git merge origin/main`

21. Add a tracking branch

`git branch --track feature origin/feature`

22. Create bare repository
23. Add remote repository

`git remote add <name> <repository>`

25. Push to remote repository

`git push <remote> main`

26. Hosting Git repositories

`git daemon --verbose --export-all --base-path=.`
`--enable=receive-pack` - enable pushing to this repository
## Git Internals

Blobs, trees and commits.

`git cat-file -t <hash>` - object type
`git cat-file -p <hash>` - object dump
## Useful commands

`git status -s` - compact output

`git diff` - show what was changed, but not staged (compares what is in your working directory with what is in your staging area)
`git diff --staged` - compares staged changes to the previous commit

`git commit -a -m "..."`

`git rm --cached <file>` - untrack file

`git log -p -2`
`git log --stat`
`git log --pretty=[oneline|full|fuller]`
`git log --pretty=format:"..."`
`git log --graph`
`git log --grep=...`
`git log --until=... --since=...`
`git log -S <s>` - show commits that change the number of occurrences of s
`git log -- <file>` - show only commits that changed file

`git restore --staged <file>...` - unstage staged file
`git restore <file>...` - discard modifications made to the file