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

## Tools
- [Git Graph Visualizer](https://git-graph.harshkapadia.me/)
- [Git Sizer](https://github.blog/2018-03-05-measuring-the-many-sizes-of-a-git-repository/)

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

## Git data model (Directed Acyclic Graph)
- https://blog.10pines.com/2018/05/21/the-model-behind-git/
- https://astahblog.com/2015/09/08/git-data-model/
- https://www.atomiccommits.io/gits-dag
- https://cloudoki.com/do-you-really-know-git/
  - > It's common to think about version history as a tree. However, in a tree, a node can only have 1 parent and there can only be 1 tree root. In a **directed acyclic graph**, a node can have any number of nodes pointing to it.
- [What's the difference between the data structure Tree and Graph?](https://stackoverflow.com/questions/7423401/whats-the-difference-between-the-data-strucdirected%20acyclic%20graphture-tree-and-graph)
- [Đồ thị có hướng - Directed và không có chu trình - Acyclic](https://viblo.asia/p/data-structures-graph-Do754OnBlM6)
- https://stackoverflow.com/questions/26395521/dag-vs-tree-using-git
- [The Architecture and History of Git: A Distributed Version Control System](https://medium.com/@willhayjr/the-architecture-and-history-of-git-a-distributed-version-control-system-62b17dd37742)
- [Git is a Directed Acyclic Graph and What the Heck Does That Mean?](https://medium.com/girl-writes-code/git-is-a-directed-acyclic-graph-and-what-the-heck-does-that-mean-b6c8dec65059)

### Notes

Things immediately `outside` **.git** comprise the **working directory**, which is an optional accomodation to make working with your Git repository easier. By default working directory reflects the latest commit of your local repository, but you can switch your working directory tree to different commits within the repository, and modify/create/delete files within the working directory before making a new commit.
