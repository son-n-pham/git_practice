# git_practice
---
This is the place to practice Git and GitHub
---
### Some Steps to Remember First:
- Create new repo in GitHub
- Get the syntax to connect the new repo with the local git directory
- In the local directory:
  - Initiate: git init
  - Check git status: git status
  - Add file to track: git add filename
  - Commit file(s): git commit -m "Description of the change"
  - Some others useful: check the different with "git diff filename" and check the change of commit with "git log (filename(s))"
  - Then use the syntax from GitHub's new repo to push the commited file into GitHub

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

 ### [Quick way to add image to MarkDown in GitHub](https://ardalis.com/add-images-easily-to-github/)
  Here are the steps to stay in GitHub in your browser and still be able to add images to your content using copy-paste. This is from the following link https://ardalis.com/add-images-easily-to-github/
- On your repository where you want to add images to markdown files, wiki pages, etc. create an Issue. Call it "Images".
  ![Issue_page](https://user-images.githubusercontent.com/79841341/124356726-3502d200-dc4a-11eb-852a-6fd6bb8b505e.png)
- Now get an image, perhaps using the Windows Snipping Tool or SnagIt, and copy it.
  ![Issue_page_before_paste_image](https://user-images.githubusercontent.com/79841341/124356764-70050580-dc4a-11eb-8b63-a408befa2ada.png)
- Paste into the body of the issue you created. You should see it upload quickly and then display markdown with a URL. Note that you can also use drag-and-drop or click on "selecting them" to upload. **We do not need to save the issue.**
![link_when_page_image](https://user-images.githubusercontent.com/79841341/124356826-cffbac00-dc4a-11eb-8126-c27383ed8097.png)
- Copy the generated markdown from the image into your markdown file or wiki page. You can of course change the generic [image] to something more reflective of the image, as this is used for the alt tag.
- Repeat as needed. You can close the issue and keep it around for additional images in the future, or just abandon it and never save it. Uploaded images on an issue that is never saved are still retained. You can also use the same trick in comments on issues, so you could easily just add one comment per image you need to add as well.
