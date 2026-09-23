# A02

Part 1 - Tutorial on setting up git/webstorm/github<br><br>
Step 1 - Install and Configure Git locally<br>
&nbsp; In the terminal run git --version<br>
&nbsp; Then run the following<br>
&nbsp; &nbsp; git config --global user.name "Your Name"<br>
&nbsp; &nbsp; git config --global user.email "your.email@example.com"<br>
&nbsp; &nbsp; git config --global init.defaultBranch main<br>
Step 2 - Create and Authenticate GitHub Remote<br>
&nbsp; Generate an ssh key by running the command: ssh-keygen -t ed25519 -C "your.email@example.com"<br>
&nbsp; &nbsp; Then copy the key by running cat ~/.ssh/id_ed25519.pub<br>
&nbsp; &nbsp; &nbsp; On github go to settings, ssh and gpg keys, then new ssh key, paste the key and save<br>
&nbsp; &nbsp; &nbsp; &nbsp; Lastly Verify the connection by running the following in your terminal ssh -T git@github.com<br><br>
Step 3 - Connect Webstorm to Git and Github<br>
&nbsp; Launch WebStorm and open Settings<br>
&nbsp; &nbsp; Navigate to Version Control -> Git: Click Test next to Path to Git executable. Make sure WebStorm detects the binary (e.g., git.exe or /usr/bin/git).<br>
&nbsp; &nbsp; &nbsp; Navigate to Version Control -> GitHub:<br>
&nbsp; &nbsp; &nbsp; &nbsp; Click the + (Add Account) icon.<br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Select Log In via GitHub... to authenticate directly via your browser.<br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Confirm your avatar and account name appear in the WebStorm account list, then click Apply and OK.<br><br>
Step 4 - Clone or Initialize a Repository in WebStorm:<br>
&nbsp; Option A: Clone an existing GitHub repository<br>
&nbsp; &nbsp; On the WebStorm welcome screen (or top menu), go to Git → Clone... (or File -> New -> Project from Version Control).<br>
&nbsp; &nbsp; &nbsp; Select GitHub on the left panel, choose your repository, define the local directory, and click Clone.<br><br>
Option B: Initialize an existing local project<br>
&nbsp; Open your project folder in WebStorm.<br>
&nbsp; &nbsp; Go to the top menu: VCS -> Enable Version Control Integration (or Git -> Create Git Repository)<br>
&nbsp; &nbsp; &nbsp; Select Git and click OK.<br>
&nbsp; &nbsp; &nbsp; &nbsp; Link to GitHub: Go to Git -> GitHub -> Share Project on GitHub, name the remote repository, choose public/private, and click Share.<br><br>
Part 2: Glossary<br>
**Branch**: Isolated lines of development within a depository that allow feature work or bug fixes without altering the production codebase<br>
**Clone**: Copy of an entire remote repository down to a local development machine.<br>
**Commit**: Snapshots of the staged changes in the repository at a given time, each commit has unique information alongside commit messages that document what changed and why<br>
**Fetch**: Downloads new commits, branches, and full commit history from a remote repository to the local git database.<br>
**GIT**: This is a version control system that tracks changes in source code over time allowing multiple developers to have full information regarding the project and the ability to make changes.<br>
**GitHub**: A cloud based hosting platform built on top of hit that provides centralized remote repository infrastructure, access control and other key features like pull requests.<br>
**Merge**: Combines the commit histories and file changes of two different branches into a single branch.<br>
**Push**: This is a git command that uploads local commits from a specific branch to the corresponding branch on a remote repository.<br>
**Pull**: This executes both a fetch and merge in sequences, retrieving changes from the remote tracking branch then integrating them directly into checked-out local branch.<br>
**Remote**: Shared, hosted version of GitHub repo used for syncing changes across environments<br>
**Repository**: A directory managed by git that houses project files alongside the revision history. They can exist locally or remotely via github.
