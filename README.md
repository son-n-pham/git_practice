# This is my collection of useful Git and GitHub tips
---
This is the place to note useful Git and GitHub
---
### Steps to Create fresh Repo in GitHub and connect to local git folder:
- Create new repo in GitHub
- Get the links to connect the new repo with the local git directory
- In the local directory:
  - Initiate: git init
  - Check git status: git status
  - Add file to track: git add filename
  - Commit file(s): git commit -m "Description of the change"
  - Some others useful: check the different with "git diff filename" and check the change of commit with "git log (filename(s))"
  - Then use the syntax from GitHub's new repo to push the commited file into GitHub

### Foreigh Github repo => local folder by git clone => own Githut repo
- Run git clone
- Run git remote rm origin
- Create new repo in Github
- Run git add origin Link_of_the_new_repo
- Run git push
  
### Undo changes:
There are couple of ways to reest our work as below:
- git reset HEAD filename: Take the filename out of staging area
- git checkout HEAD filename: Discard changes in the working directory
- git reset commit_SHA: reset to previous commit with its 7-digit commit_SHA. This is to reset the HEAD to the specific commit; however, the change is still on the working directory. Need to run Git checkout HEAD filename to discard changes in the working directory and back to the previous commit.

HEAD commit is the commit that we are currently on.

### git branch:
- git branch: Check what branch we are currently on. Branches have commits of master and commits which master does not have.
- git branch new_branch: To create new_branch
- git checkout branch_name: To switch to branch_name
- git merge branch_name: To merge branch name to master. We need to have git checkout master to back to master first.
- git branch -d branch_name: To delete branch_name

### git Teamwork
- git clone remote_location clone_name:
  - remote_location: can be a web adress or filepath
  - clone_name: the name we give to the directory which Git will clone the repo into. clone_name is the local copy of the remote_location Git project. Whatever we commit in clone_name, the owner of the origin remote_location will not know about those commits.
- git remote:
  - **git remote add origin "Link of the git repo"** // This is to connect our local drive to github page
  - git remote -v: To see the list of Git project's remotes. Behind the scene, Git gives the remote_location the name origin to refer it more conveniently.
- git fetch: to update the repo from remote. After git fetch, we need to run git merge origin/master to merge the fetching with the local master.
- Create a branch to work on a new project feature
- Develop feature in the branch, commit work
- Fetch and merge from the remote again (In case the remote have some update while we are working)
- git push origin <branch_name>: Push our branch_name to the remote for review.
- git push -f <remote> <branch>: Override github repo with local files/folders

### Some Steps to Remember First:
- Create new repo in GitHub
- Get the syntax to connect the new repo with the local git directory
  - git init
  - Check git status: git status
  - Add file to track: git add filename
  - Commit file(s): git commit -m "Description of the change"
- git remote:
  - git remote origin "Link of the git repo" // This is to connect our local drive to github page

 ### Quick way to add image to MarkDown in GitHub (Updated)
 This is the most convenient way that I found out and usually apply.
  
#### From image with link: Just use the syntax
  ```Markdown
  ![Description_of_image](link of the image)
  ```
  
#### From copied image by screenshot:
  - Step 1: Copy image by screenshot or existing image by Ctrl+C
  ![image](https://user-images.githubusercontent.com/79841341/126900678-5951dbd7-01dd-41b3-90a1-8af81b248952.png)
  
  - Step 2: Paste directly to GitHub Markdown editing box. GitHub generate link of the image.
  ![image](https://user-images.githubusercontent.com/79841341/126900698-da97ffe1-ce63-49aa-ab17-38a30360fb9d.png)
  
    ![image](https://user-images.githubusercontent.com/79841341/126900730-8f0299ce-6350-4789-bbde-140148dce0f1.png)
  
  - Step 3: Commit the change to check the image in the view mode.
  
### How to fork a repo
- Fork the target in its Github page
- Download the forked project into the local folder by git clone
- Setting the project upstream to update from the parent repo.
  - Get the parent HTTPS link.
  - Use: git remote add upstream <The copied HTTPS>
  - We can update that our forked repo by: git fetch upstream
