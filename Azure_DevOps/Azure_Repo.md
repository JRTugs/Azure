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


## Creating New Repository and uploading Repository from local to Azure Repo
**1. Create Repository**

On Dropdown on Top > Click New Repository

<img width="404" alt="image" src="https://github.com/user-attachments/assets/12bd0f5c-8e90-4e57-8b2e-a98df5a77d92">


On create a Repository Window, Fill in Repository Name > Click "Create"

<img width="227" alt="image" src="https://github.com/user-attachments/assets/4970f48d-8bbc-434d-bb85-818185795ac3">

**2. Clone New Repistory created from Azure Repo**

Click "Clone" on top right

<img width="785" alt="image" src="https://github.com/user-attachments/assets/9506a107-5b7e-4721-bf5b-06005663d33d">

Click Generate Git Credentials 

<img width="226" alt="image" src="https://github.com/user-attachments/assets/9ffe2d1b-0b1d-491e-9a99-c3601f0da6ea">

Copy all details

<img width="223" alt="image" src="https://github.com/user-attachments/assets/fa916e10-c0cc-4acd-bc32-4951f826c876">

Run below command on local server to clone Azure repo locally

```bash
mkdir azurerepo && cd azurerepo
git clone https://nojazuredevopsdemo@dev.azure.com/nojazuredevopsdemo/helloworld/_git/hello-world
```

Verify hello-world directory is cloned

<img width="339" alt="image" src="https://github.com/user-attachments/assets/a9deadc8-1c2a-4de8-8111-170943cd57eb">


**3. Copy files to azurerepo directory and push to Azurerepo**

Copy Files to hello-world directory

```bash
cp -a helloworld/* azurerepo/hello-world/
```

Note: Only copy source code. If there is a .git directory, it should not be copied

Add the new files

```bash
git add .
```

Commit added files
```bash
git commit -m "Initial Commit"
```

Push new files to Azure Repository
```bash
git push
```

**4. Verify from Azure repo**

<img width="313" alt="image" src="https://github.com/user-attachments/assets/e755b73c-df4c-4cc8-ab63-d6f342b6431a">




