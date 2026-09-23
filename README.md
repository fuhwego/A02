# A02

Part 1 - Tutorial on setting up git/webstorm/github

Step 1 - Install and Configure Git locally
  In the terminal run git --version
  Then run the following 
    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"
    git config --global init.defaultBranch main
Step 2 - Create and Authenticate GitHub Remote
  Generate an ssh key by running the command: ssh-keygen -t ed25519 -C "your.email@example.com"
    Then copy the key by running cat ~/.ssh/id_ed25519.pub
      On github go to settings, ssh and gpg keys, then new ssh key, paste the key and save
        Lastly Verify the connection by running the following in your terminal ssh -T git@github.com

Step 3 - Connect Webstorm to Git and Github
  Launch WebStorm and open Settings
    Navigate to Version Control -> Git: Click Test next to Path to Git executable. Make sure WebStorm detects the binary (e.g., git.exe or /usr/bin/git).
      Navigate to Version Control -> GitHub:
        Click the + (Add Account) icon.
          Select Log In via GitHub... to authenticate directly via your browser.
            Confirm your avatar and account name appear in the WebStorm account list, then click Apply and OK.

Step 4 - Clone or Initialize a Repository in WebStorm:
  Option A: Clone an existing GitHub repository
    On the WebStorm welcome screen (or top menu), go to Git → Clone... (or File -> New -> Project from Version Control).
      Select GitHub on the left panel, choose your repository, define the local directory, and click Clone.

Option B: Initialize an existing local project
  Open your project folder in WebStorm. 
    Go to the top menu: VCS -> Enable Version Control Integration (or Git -> Create Git Repository)
      Select Git and click OK.
        Link to GitHub: Go to Git -> GitHub -> Share Project on GitHub, name the remote repository, choose public/private, and click Share.
  
Part 2: Glossary 
**Branch**: Isolated lines of development within a depository that allow feature work or bug fixes without altering the production codebase
**Clone**: Copy of an entire remote repository down to a local development machine.
**Commit**: Snapshots of the staged changes in the repository at a given time, each commit has unique information alongside commit messages that document what changed and why
**Fetch**: Downloads new commits, branches, and full commit history from a remote repository to the  local git database.
**GIT**: This is a version control system that tracks changes in source code over time allowing multiple developers to have full information regarding the project and the ability to make changes.
**GitHub**: A cloud based hosting platform built on top of hit that provides centralized remote repository infrastructure, access control and other key features like pull requests.
**Merge**: Combines the commit histories and file changes of two different branches into a single branch.
**Push**: This is a git command that uploads local commits from a specific branch to the corresponding branch on a remote repository.
**Pull**: This executes both a fetch and merge in sequences, retrieving changes from the remote tracking branch then integrating them directly into checked-out local branch.
**Remote**: Shared, hosted version of GitHub repo used for syncing changes across environments 
**Repository**: A directory managed by git that houses project files alongside the revision history. They can exist locally or remotely via github.
