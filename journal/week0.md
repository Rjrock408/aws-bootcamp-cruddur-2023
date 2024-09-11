# Week 0 — Billing and Architecture

Installing AWS CLI

![image](https://github.com/user-attachments/assets/76986645-ee86-4ee1-ba2a-626c8eea1531)
![image](https://github.com/user-attachments/assets/00ac6e0f-c9f0-4bb0-bd2f-773345e72835)


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


