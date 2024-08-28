# Azure Repository

## Cloning repository from Github to Azure Repo
**1. Create Personal Access Token**

Click "Profile Icon" on top right > Click "Settings"

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/d8a7fb65-d328-4b3c-9f0a-e5cb773a9881)

Settings, Click on "<>Developer settings" on the bottom
    
  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/8136f9e6-c5d8-4255-85a5-23277ffc05eb)

On Developer Settings, Click "Personal access tokens", Click "Tokens (Classic)" and Click "Generate new token (classic)"

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/774df725-ff0d-462a-80f8-6ff72a95a29a)

On New personal access token window, Put a note

Set expiration as desired

Check all execpt (delete_repo and delete:packages)

Once completed, Click "Generate token"

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/578316a4-6536-4cd4-ad89-d55fe0c29a99)
  
```bash
Note: Make sure to copy your personal access token now. You won’t be able to see it again!
```

New Token Generated

![image](https://github.com/user-attachments/assets/2f9272ee-961d-4488-9a6b-aaf89cc5e077)

**2. Import a Git Repostiry to Azure Repo**

On Azure DevOps > Clicl Repos > Click the Dropdown on Top > Click Import Repoistory

<img width="490" alt="image" src="https://github.com/user-attachments/assets/c289b565-89ac-44f9-8309-ac787a794bdf">

On Import a Git Repository:

1. Select Git
2. Fill in the Clone URL from Github
3. Fill in Username
4. Fill in Personal Access Token
5. Fill in Repo Name

Once Done Click Import

<img width="235" alt="image" src="https://github.com/user-attachments/assets/73b90e44-9b7f-49eb-a344-37a0223a15b9">

**3. Confirm Repository uploaded**

<img width="533" alt="image" src="https://github.com/user-attachments/assets/353133cf-e588-402b-bc4d-6914e6251aa3">

  
