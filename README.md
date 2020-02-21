## First section: You must explain the difference between cloning vs fetching vs pulling. Give real world examples of how they differ.

> **Git Clone** - Targets an existing repository and copies it. Non collaborators cannot make changes to the project and for those who are collaborators, all operations are managed through the local repository. Ideal for projects that are already set up and I just want a developmental copy of the project.

> **Git Fetch** - Fetches new data from a repository; however, it does not combine any of this data into your working files. Ideal for when I am acquiring a new overview of what is happening in a repository.

> **Git Pull** - Similar to git fetch; however, in addition to downloading the new data from a repository, git pull combines it into your current working files. This is ideal if I was updating your current branch with the latest changes from the remote server.

## Second section: Create a markdown table that shows the basic differences between Trello and Asana. The list does not need to be exhaustive. Make sure to use a table.

| Trello          | Asana          |
| --------------- | -------------- |
| Card Based      | Non-Card Based |
| No Chat Option  | Chat Option    |
| No File Sharing | File Sharing   |
| No Task Nesting | Task Nesting   |
| Board Overview  | Task Overview  |

## Third Section: Answer the following 3 questions:

_Question 1: What is the .git folder? Where is the object database in this folder?_

The .git folder contains a log that stores the commits that you make and a history of it. In addition, the .git folder also contains all the information that is required for your project in version control and remote repository address. As shown below, the object database is in the HEAD.

.git

├── HEAD
├── branches
├── config
├── description
├── hooks
│ ├── pre-commit.sample
│ ├── pre-push.sample
│ └── ...
├── info
│ └── exclude
├── objects
│ ├── info
│ └── pack
└── refs
├── heads
└── tags

_Question 2: Explain in detail how the git hash-object function works._

> Whenever a file is added, you get a hash generated on the content. This hash is used to identify that version of a file. The hash could look like like47a265fb5b5709b0121d3987a091960525becfda. This hash is one way, meaning that we cannot convert this back to the original input. In addition, the length of the hash is always fixed and the same input will always produce the same hash. Hash functions vary from MD5, SHA1, SHA256, SHA384, or SHA512.

_Question 3: Where does git internally store the file names to our files? How are tree objects related to this?_

> Git internally stores our files as BLOBS (binary large object). This is the object type used to store the contents of each file in a repository. The file's SHA-1 hash is computed and stored in the blob object and allow you to read and write BLOB objects to your git database. BLOBS DO NOT store metadata like file names.

> Tree objects used created with git mktree and not git hash-object. The tree objects stores information about our git directories. Trees could be comprised of a set of BLOBS or in addition to other trees. Similar to directories and sub-directories in our computer, which forms a tree.

> I added this to fix an issue.

When you are finished answering these questions, create an issue called "readme updates" and open a pull request for this gitfundamentals branch. Make sure that when you merge the branch ... the issue automatically closes.

Don't forget all the "best practices" we have discussed this term.
