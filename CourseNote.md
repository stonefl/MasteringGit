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
`git config --user.name "your name"`

`git config --user.email "your email"`

To check all your settings:

`git config --list` 


# Section 3 The Git workflow under a microscope

* Quickly create a file from the command line
  * Linux: `touch newFile`
  * Windows: `copy con newFile`