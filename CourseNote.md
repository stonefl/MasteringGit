# Section 1 Keeping Software Under Control

## Section 1.1 Understanding Version Control

**What is version control?**

* Writing software is an iterative process
* Involves changes - often simultaneously from multiple developers
* Version control provides a means to
   * Manage changes
   * Develop a "historical" view of the project
* A multi-faceted tool
   * A common data store for the project's code
   * Share updates and changes with others
   * Maintain a history of the project's evolution
   * Provide the freedom to explore and experiment
   
**Source Control Management(SCM)**

* A "Database of Changes"
   * Tracks changes and who made them
   * Automatically merges changes
   * Helps resolve "conflicts" in merges when arise
* SCM systems fall into two basic categories:
   * Centralized
     * Eevery user **MUST** be connected to the central server
     * Entire history of the project **ONLY** on the central server
     * Updates require a 'Check-in' and 'Check-out' process
   * Distributed
     * Does not require a central server
     * With Git, every user has a copy of the entire history(locally)
     * Updates are all 'locally' managed

**Distributed Source Control**

* Some advantages of distributed SCM (like Git)
  * Implicit redundancy
  * Quicker, uninterrupted workflow
  * Common operations are faster
  * Simpler branching and merging
  * No reliance on a centralized server
  * Simple to set-up
  * More freedom for developers
  * The project history may be stored on a remote server with a distributed SCM

# Section 2 Let's Git Started

## Section 2.1 Using Git with Nitrous

* Create an account on Nitrous.io

## Section 2.2 Verify your Git installation and version

* verify presence of Git and its version through: `git-version`

## Section 2.3 Setting up globals

`git config --global user.name "your name"`

`git config --global user.email "your email"`

To check all your settings:

`git config --list` 


# Section 3 The Git workflow under a microscope

* Quickly create a file from the command line
  * Linux: `touch newFile`
  * Windows: `copy con newFile`

## Section 3.1 Typical Git workflow

* Write some code
* Add new files
* Commit changes with `git commit -am "commit message"`
* Repeat

**Status Options** `git status -sb`

* `-s`: short format
* `--long`: long format(**default**)
* `-b`: includes branch and tracking, even when used with short format
* `- u no`: hides untracked files in the directory
* `-u normal`: includes untracked files in the directory(**default**)
* `-u all`: adds all files in untracked directories (a bit verbose)
* `--ignored`: include ignored files
* `--column`: displays untracked files in columns
* `-- no-column`: untracked files in a list (**default**)
* `--porcelain`: primarily intended to be consumed by scripts

## Section 3.2 Setting the Stage

**Staging process**

* Changes are captured in the "index"
   * Changes that will become part of the next commit
   * Adding changes to the index is known as 'staging'

* Command `git add`
  * Stages all changes
     * Added
     * Modified
     * Deleted
     
 * Options of `git add`
    * `git add -A` stages All in entire working directory
    * `git add -u` modified and deleted, without new
    * `git add .` stages all in current directory
     
 **Example**
 
 `touch changedFile`
 `touch deletedFile`
 `git add changedFile deletedFile`
 `git status`
 `git commit -m "Staging Exercise"`

make some changes
`echo CHANGES  >> changedFile`
`rm deletedFile`
`echo I am new > addedFile`
`git status`
`git add .`

Undo changes
`git reset`

`touch gitAdd`
`git status`
`git add -u`
`git add -A`
`git status`

## Section 3.3 The Commit

edit a file thorugh vim:
`vi README.md`
`git status`
`git commit -am "updated README.md"`
`git log --pretty=fuller`
`man git commit` to open git commit manual

* Commit command modifiers:
  * `-a`, `--all` stage modified/deleted files ignoring any not added
  * `amend` replace or update the last commit you made
  * `-o`, `--only`commit only from paths specified on the command line
      * this disregards any staged files
      * it is the default mode if a path is included in the command line
  * `-v`, `verbose` provides a diff in the commit message template
  * `-F "file"`, `--file="file"` use text from "file" as commit message
  * `-m "msg"`, `--message="msg"` commit message
       * multiple `-m` options are concatenated as separate paragraphs
       

