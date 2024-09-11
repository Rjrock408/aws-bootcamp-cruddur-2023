# Week 0 — Billing and Architecture

Installing AWS CLI

![image](https://github.com/user-attachments/assets/76986645-ee86-4ee1-ba2a-626c8eea1531)

AWS CLI references:
https://docs.aws.amazon.com/cli/latest/reference/

installin awscli in your local system(linux)
![image](https://github.com/user-attachments/assets/2960d4ae-1bd7-4747-8dcc-3208962e528d)

installing on local env.(https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install --bin-dir /usr/local/bin --install-dir /usr/local/aws-cli --update

Linux env. variables::
echo $PATH

SET environment variables for local machine

Update our .gitpod.yml to include the following task.

```
tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
```


HOW to create a new branch in the git repo::
https://graphite.dev/guides/git-commit-to-new-branch
    Create a new branch with git checkout -b new-feature
    Add changes to your new branch with git add
    Commit your changes with git commit -m "Your message"
    Push your branch to a remote with git push -u origin new-feature

Step 1: Create a new branch:
```git checkout -b new-feature```
Create a new branch and keep your staged changes
```git checkout -b new-feature```
If you have changes already staged (using git add), and you want to move these to a new branch

Step 2: Add changes to the new branch::

```git add <file-or-directory>```

Step 3: Commit the changes::

```git commit -m "Add a descriptive message here"```

Step 4: Push the new branch to a remote repository
Check if the remote exists

Before pushing, check if the remote repository is set up:
```git remote -v```

```git remote add origin <repository-url>```

Push the new branch to the remote repository

```git push -u origin new-feature```


![image](https://github.com/user-attachments/assets/0e9d8213-b107-44f0-81a8-18c343ac3144)












