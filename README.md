# a-little-bit-about-git

## git-story
- https://www.freecodecamp.org/news/animate-your-git-repo-with-git-story/

## DIY
- https://wyag.thb.lt/#orgf45a226

## Git internals
- https://www.youtube.com/watch?v=ADvD-DfSTSU
- [Git Object Model](http://shafiul.github.io/gitbook/1_the_git_object_model.html)
- ### Hardcore
  - https://medium.com/swimm/a-visualized-intro-to-git-internals-objects-and-branches-68df85864037
  - https://medium.com/swimm/getting-hardcore-creating-a-repo-from-scratch-cc747edbb11c

## Visualizer Tools
- https://git-graph.harshkapadia.me/

## [Structures](https://stackoverflow.com/a/56026788/10393067)
**.git** is initialized by `git init`.

**.git** contains all information required for version control. If you want to clone your repo, copy **.git** is enough.

4 sub-directories:

- **hooks/** : Git hooks are the scripts that are executed before or after events like commit, push etc.
- **info/** : `exclude` file for ignored patterns
- **objects/** : This folder represents an object database of Git. All "objects"
- **refs/** :  This folder stores information about tags and branches. Pointers to commit objects

4 files:
- **HEAD** : current branch. It points to the master branch by default.
- **config** : configuration options
- **description**
- **index** : staging area. This is a binary file and stores staging information.


Here "object" includes:

- **blobs** (files)
- **trees** (directories)
- **commits** (reference to a tree, parent commit, etc)

The **.git** folder is hidden to prevent accidental deletion or modification of the folder. The version history of the code base will be lost if this folder is deleted. This means, we will not be able to rollback changes made to the code in future.

### Notes

Things immediately `outside` **.git** comprise the **working directory**, which is an optional accomodation to make working with your Git repository easier. By default working directory reflects the latest commit of your local repository, but you can switch your working directory tree to different commits within the repository, and modify/create/delete files within the working directory before making a new commit.
