# task-1
## Version control
version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. For this examples, you will use software source code as the files being version controlled, though in reality you can do this with nearly any type of file on a computer.
If you are a graphic or web designer and want to keep every version of an image or layout (which you would most certainly want to), a Version Control System (VCS) is a very wise thing to use. It allows you to revert selected files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using a VCS also generally means that if you screw things up or lose files, you can easily recover. In addition, you get all this for very little overhead.

### Local Version Control Systems
 Many people’s version-control method of choice is to copy files into another directory (perhaps a time-stamped directory, if they’re clever). This approach is very common because it is so simple, but it is also incredibly error prone. It is easy to forget which directory you’re in and accidentally write to the wrong file or copy over files you don’t mean to.To deal with this issue, programmers long ago developed local VCSs that had a simple database that kept all the changes to files under revision control. One of the most popular VCS tools was a system called RCS, which is still distributed with many computers today. RCS works by keeping patch sets (that is, the differences between files) in a special format on disk; it can then re-create what any file looked like at any point in time by adding up all the patches.
 
### Centralized Version Control Systems 
 The next major issue that people encounter is that they need to collaborate with developers on other systems. To deal with this problem, Centralized Version Control Systems (CVCSs) were developed. These systems (such as CVS, Subversion, and Perforce) have a single server that contains all the versioned files, and a number of clients that check out files from that central place. For many years, this has been the standard for version control. This setup offers many advantages, especially over local VCSs. For example, everyone knows to a certain degree what everyone else on the project is doing. Administrators have fine-grained control over who can do what, and it’s far easier to administer a CVCS than it is to deal with local databases on every client. However, this setup also has some serious downsides. The most obvious is the single point of failure that the centralized server represents. If that server goes down for an hour, then during that hour nobody can collaborate at all or save versioned changes to anything they’re working on. If the hard disk the central database is on becomes corrupted, and proper backups haven’t been kept, you lose absolutely everything — the entire history of the project except whatever single snapshots people happen to have on their local machines. Local VCSs suffer from this same problem — whenever you have the entire history of the project in a single place, you risk losing everything.

### Distributed Version Control Systems 
 This is where Distributed Version Control Systems (DVCSs) step in. In a DVCS (such as Git, Mercurial or Darcs), clients don’t just check out the latest snapshot of the files; rather, they fully mirror the repository, including its full history. Thus, if any server dies, and these systems were collaborating via that server, any of the client repositories can be copied back up to the server to restore it. Every clone is really a full backup of all the data. Furthermore, many of these systems deal pretty well with having several remote repositories they can work with, so you can collaborate with different groups of people in different ways simultaneously within the same project. This allows you to set up several types of workflows that aren’t possible in centralized systems, such as hierarchical models.


## Difference between git and github 
Git is a version control system that helps manage and track changes in source code during software development. It's a distributed system that allows multiple developers to collaborate on a project.

GitHub, on the other hand, is a web-based platform that utilizes Git for version control. It provides a centralized location for hosting and sharing Git repositories, making collaboration easier. GitHub offers additional features like issue tracking, pull requests, and project management tools.

In summary, Git is the version control system, while GitHub is a platform that uses Git for collaborative software development.


## Three other GitHub alternatives 
GitLab: Similar to GitHub, GitLab is a web-based platform that provides version control using Git. It offers features like continuous integration, project management, and more. GitLab can be self-hosted or used as a cloud service.
Bitbucket: Owned by Atlassian, Bitbucket is another alternative. It supports both Git and Mercurial for version control. Bitbucket provides features like pull requests, code collaboration, and integration with other Atlassian tools.
SourceForge: SourceForge is a web-based platform that supports version control systems like Git, Mercurial, and Subversion. It offers project hosting, collaborative tools, and a platform for open-source software development.


## Difference between git fetch and git pull
‘Git fetch and git pull’ are both Git commands, but they serve different purposes.
Git fetch: This command retrieves changes from a remote repository but doesn't automatically merge them into your local branch. It's useful for inspecting changes before deciding to merge. After fetching, you can use ‘git diff’ or other commands to review the changes. Fetching allows you to see the updates without affecting your working directory.
Git pull: This command, on the other hand, fetches changes from a remote repository and automatically merges them into your current branch. It's essentially a combination of ‘git fetch’ and ‘git merge’. Git pull is convenient when you want to quickly update your local branch with changes from the remote repository.
In summary, ‘git fetch’ is more about retrieving changes for inspection, while ‘git pull’ is a shortcut that fetches and merges changes into your local branch in one step.


## Git rebase and the command for it 
In simple terms, ‘git rebase’ is a command used to change the base of your current branch. It's like rewriting the history of your changes to make it cleaner and more straightforward.
###Command:
The basic command for git rebase is ;  git rebase <branch_name> 


## Git cherry-pick and the command for it 
In simple terms, ‘git cherry-pick’ is a command that allows you to pick and apply specific commits from one branch and apply them onto another branch. It's like selecting and copying individual changes.

### Here's a basic idea:
Selecting Specific Commits:
If you have a commit on one branch that you want on another, you can use ‘git cherry-pick’ to grab just that commit.
#### Commands:
The basic command for ‘git cherry-pick’ is : 
git cherry-pick <commit_hash>

















