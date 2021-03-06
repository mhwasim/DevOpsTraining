# DevOpsTraining

Methods of Git Reset

1. Hard:
========
makes everything match the commit you've reset to. This is the easiest to understand, probably. All of your local changes get clobbered. One primary use is blowing away your work but not switching commits: git reset --hard means git reset --hard HEAD, i.e. don't change the branch but get rid of all local changes. The other is simply moving a branch from one place to another, and keeping index/work tree in sync. This is the one that can really make you lose work, because it modifies your work tree. Be very very sure you want to throw away local work before you run any reset --hard.

2. Mixed:
=========
It is the default, i.e. git reset means git reset --mixed. It resets the index, but not the work tree. This means all your files are intact, but any differences between the original commit and the one you reset to will show up as local modifications (or untracked files) with git status. Use this when you realize you made some bad commits, but you want to keep all the work you've done so you can fix it up and recommit. In order to commit, you'll have to add files to the index again.

3. Soft:
========
It doesn't touch the index or work tree. All your files are intact as with --mixed, but all the changes show up as changes to be committed with git status (i.e. checked in in preparation for committing). Use this when you realize you've made some bad commits, but the work's all good - all you need to do is recommit it differently. The index is untouched, so you can commit immediately if you want - the resulting commit will have all the same content as where you were before you reset.

4. Merge:
=========
Was added recently, and is intended to help you abort a failed merge. This is necessary because git merge will actually let you attempt a merge with a dirty work tree (one with local modifications) as long as those modifications are in files unaffected by the merge. git reset --merge resets the index (like --mixed - all changes show up as local modifications), and resets the files affected by the merge, but leaves the others alone. This will hopefully restore everything to how it was before the bad merge. You'll usually use it as git reset --merge (meaning git reset --merge HEAD) because you only want to reset away the merge, not actually move the branch. (HEAD hasn't been updated yet, since the merge failed)

------------------------------------------------------------------------------------------------
Stages of Git 
Untracked:
==========
a. the file exists, but is not part of Git's version control

Modified:
=========
a. making some additions to the original files tracked by Git

Staged:
=======
a. the file has been added to git's version control but changes have not been committed

Committed at Local Repository:
==============================
a. the change has been committed

Push at Remote Repository:
==========================
a. Uploading the commits from local Git repository to remote repository
------------------------------------------------------------------------------------------------
Difference between Git and GitHub
Git is a version control system that lets you manage and keep track of your source code history
GitHub is a cloud-based hosting service that lets you manage Git repositories

Git is a free, open-source software distributed version control system (DVCS) designed to manage all source code history
GitHub offers all of Git???s DVCS SCM and has some additional features. This includes collaboration functionality like project management, support ticket management, and bug tracking

Git is installed locally on a system, so developers can manage their source code history using their local machines as repositories
GitHub is a cloud based, so Internet access is required. It also has a built-in user-management system and a user-friendly GUI

Git can be used without GitHub
GitHub cannot be used without Git

Git is an open-source tool since it was first released in 2005 and maintained by the Linux Foundation
GitHub was launched as a company in 2008 and acquired by Microsoft in 2018
------------------------------------------------------------------------------------------------
What are the benefits of Cloud Computing
1. Reduced IT Costs:
====================
a. The cost of system upgrades, new hardware and software may be included in your contract
b. No longer need to pay wages for expert staff
c. Energy consumption costs may be reduced
d. There are fewer time delays

2. Accessibility:
=================
a. Can be accessed from anywhere if internet is available

3. Reliability:
===============
a. Can always get instantly updated about the changes

4. Scalability:
===============
a. Buy resources according to the need
b. Can scale up the resources bought
c. Can scale down the resources bought

5. Business Continuity:
=======================
a. In case of disaster backup restored
b. Minimal downtime and loss of productivity

6. Enable Mobility:
===================
a. Gives businesses the ability to enable employees to gain access to data and applications from anywhere
b. Making employees more productive when on the go

7. Access to Automatic Updates:
===============================
a. May be included in your service fee
b. Depending on your cloud computing service provider, your system will regularly be updated with the latest technology
------------------------------------------------------------------------------------------------
Define Continuous Integration, Continuous Delivery & Continuous Deployment

Continuous Integration:
=======================
1. Merge changes back to the main branch as often as possible. 
2. Changes are validated by creating a build and running automated tests against the build. 
3. This is to avoid integration challenges that can happen when waiting for release day to merge changes into the release branch.
4. Emphasis on testing automation to check that the application is not broken whenever new commits are integrated into the main branch.

Continuous Delivery:
====================
1. An extension of continuous integration because it automatically deploys all code changes to different environments like testing, hotfix, production after the build stage. 
2. An automated release process you can deploy your application any time by just clicking a button.
3. Can decide to release daily, weekly, fortnightly, or whatever suits your business requirements. 
4. If truly want to get the benefits of continuous delivery, should deploy to production as early as possible to make sure that release in small batches that are easy to troubleshoot in case of a problem.

Continuous Deployment:
======================
1. One step further than continuous delivery. With this practice, every change that passes all stages of the production pipeline is released to the customers. 
2. There's no human intervention
3. Only a failed test will prevent a new change to be deployed to production.
4. An excellent way to accelerate the feedback loop with customers and take pressure off the team as there isn't a Release Day anymore. 
5. Developers can focus on building software, and they can see their work go live minutes after they've finished working on it.
------------------------------------------------------------------------------------------------
Agile & DevOps

Agile is an iterative approach to project management and software development that focuses on collaboration, customer feedback, and rapid releases. It arose in the early 2000s from the software development industry, helping development teams react and adapt to changing market conditions and customer demands.

DevOps is an approach to software development that enables teams to build, test, and release software faster and more reliably by incorporating agile principles and practices, such as increased automation and improved collaboration between development and operations teams. Development, testing, and deployment occur in both agile and DevOps. Yet traditional agile stops short of operations, which is an integral part of DevOps. 

DevOps is not a replacement. But, it is a direct successor to Agile. Similar to how with time, practices get better; over time, Agile has also grown its challenges, and DevOps has turned out to be the more optimized practice.


Agile vs DevOps
Agile emphasizes collaboration between developers and product management.
DevOps includes the operations team as well.

Agile centers the flow of software from ideation to code completion.
DevOps extends the focus to delivery and maintenance.

Agile emphasizes iterative development and small batches.
DevOps focuses more on test and delivery automation.

Agile adds structure to planned work for developers.
DevOps incorporates unplanned work common to operations teams.

Goal of Agile is to improve the speed and quality of software development.
Goal of DevOps is to improve the speed and quality of software development.

Agile was a natural replacement to Waterfall model and other Scrum practices.
DevOps is not a replacement of Agile but, it is a direct successor to Agile.