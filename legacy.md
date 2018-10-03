A step by step guide on preparing and submitting a pull request
SEYEDK edited this page on OCT 3 2018 · 2 revisions
Adhering to this process is the best way to get your work included in the project:

Fork the project, clone your fork, and configure the remotes:

# Clone your fork of the repo into the current directory
git clone https://github.com/<your-username>/pcl.git
# Navigate to the newly cloned directory
cd pcl
# Assign the original repo to a remote called "upstream"
git remote add upstream https://github.com/seyedk/friendship.git
Run the unit tests. If you added new functionality, extend existing test cases or add new ones. 

If you cloned a while ago, get the latest changes from upstream:

git checkout master
git pull upstream master
Create a new topic branch (off the main project development branch) to contain your feature, change, or fix:

git checkout -b <topic-branch-name>
Commit your changes in logical chunks. For any Git project, some good rules for commit messages are

the first line is commit summary, 50 characters or less,
followed by an empty line
followed by an explanation of the commit, wrapped to 72 characters.
See a note about git commit messages for more.

The first line of a commit message becomes the title of a pull request on GitHub, like the subject line of an email. Including the key info in the first line will help us respond faster to your pull.

If your pull request has multiple commits which revise the same lines of code, it is better to squash those commits together into one logical unit.

But you don't always have to squash — it is fine for a pull request to contain multiple commits when there is a logical reason for the separation.

Push your topic branch up to your fork:

git push origin <topic-branch-name>
Open a Pull Request with a clear title and description.

After your Pull Request is away, you might want to get yourself back onto master and delete the topic branch:

git checkout master
git branch -D <topic-branch-name>