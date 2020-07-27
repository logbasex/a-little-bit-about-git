touch readme.md
git add readme.md
git commit -m 'init docs'
git rm --cached readme.md
git status

git rm -r --cached <file>: remove from local repository (.git folder) and keep working directory intact.
git reset HEAD <file>: remove file from current index (staging area)
