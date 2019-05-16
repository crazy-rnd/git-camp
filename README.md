# git-camp

### How to upload a file more than 25 MB

1. In order to upload a large file, you need to install a Git extension called Git Large File Storage (LFS). You can download 
it from this link (https://git-lfs.github.com/).

2. After download and install the extension, go to the local repository from where you upload the large file in remote repository.

3. Run the command **"git init"** in git bash or windows cli to initialize.

4. Run the command **"git lfs install"** to check if the extension is installed properly. You will get the message "Git LFS initialized"

5. If it is installed properly, then run the command "git lfs track "*.file type extension". For example, if you want to upload a pdf file then run **"git lfs track "*.pdf"**. Then only pdf files from the local repository will be added to the remote repository.

6. Then run the command **"git add .gitattributes"**. It will create a .gitattribute.txt" file in your local repository where you will
see the  line "*.pdf filter=lfs diff=lfs merge=lfs -text" since I am uploading pdf files only.

7. Then use the following genric git commands to upload the files--
  
   - **git add --all/ git add "filename"**
  
   - **git commit -m "first commit"**
   
   - **git remote add origin https://github.com/crazy-rnd/git-camp.git**
   
   - **git push -u origin master /  git push -u origin master --force**
   
 Sometimes, it may give error after executing the last command. Therefore, you can use --force attribute while pushing to the remote repository.


### How to remove/delete all files from remote repository

 --Go to the local repository and run the following commands.
 
 --**git pull**
 
 --**git rm -r * **
 
 --**git commit -m "Deleting all files"**
