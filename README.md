# Gitting started.
Welcome to the LugerLab Github page!
This Github page is organized into repositories (or repos) of scripts relating to different projects in the lab. If you are looking for a piece of software first look for the related repo, then read through the README file for more information.

## LugerLab repos are composed of the following:    
- LICENSE
    - outlines the permissions and usage information attributed to the repo in question
    - the MIT LICENSE like the one in this repo allow for anyone to freely use the software, more restrictive licenses can be applied, seek legal counsal for more information.
- README.md file includes:
    - outline of the purpose of the repo 
    - list of software included in the repo with brief descriptions
    - installtion instructions, including required dependencies
    - detailed software usage instructions (examples are good)
    - common troubleshooting guide
- travis.yml file
    - this file will run tests of the software to ensure that it isn't broken anytime the repo is updated
    - is also linked to your Travis profile
    - needs to include both functional and unti tests
- software files
    - these can be written in whatever langauge the author chooses (Python, R, MatLab ect.)
    - need to be concise and easily understandable, annotation within code is expected        

## Using LugerLab software.
1. **Cloning** In order to use software from Github you need to 'clone' the repo (aka copy the folder containing the program). 
    - There should be a green button that says 'Clone or download', click on it and copy the url. 
    - Navigate to the directory on your local machine you'd like to put this repo in. 
    - Clone it into that directory.
    
            git clone <copied_url_from_Github>

2. **Pullilng** Anytime you use the software, it could have been updated since you cloned it. To ensure you have na updaed version pull the new version.

        git pull
        
3. **Installation** To use any piece of software you'll need to make sure your machine has all the dependencies on which the software relies. Follow the README instructions for that software to install.

4. Use the software and cite its authors whenever appropriote. 


## Contributing.            
1. There are two main ways to start a new repo:
    - The easiest way is to simply use the 'New' button on the LugerLab mainpage, create the repo, and clone it into the loaction of your choosing on your local machine.
    - Conversely, you can navigate into a folder on your local machine and use: 
    
            git init
            git remote add origin git@github.com:username/new_repo
            git push -u origin master
    
2. Either way you've chosen to start a repo you will need to add each of the four file types outlined above. 
3. Now that you've got your repo set up you can start editing your software.
    - The first thing you need to do is make sure your local master branch is up to date with the remote master (files on Github)
            
            git pull origin master
            
    - Now, you can create a new branch to work in. This is important because directly editing master branches can lead to irreversible changes. This command will create a new branch and 'checkout' it (think checking out a library book).
    
            git checkout -b <new_branch>
            
    - Any edits you make now will be in your new_branch, not your master branch. You can use 
    
            git checkout <branch_name>
            
      to move between different branches. Now you can make some edits to your software.
    - Once you've made some edits, save your file and add the editied (or new) file to a commit (think adding a comment in your library book).

            git add <file_name>
            
    - A commit is a group of changes you would like to add to the master file (think marking up your checked out library book). Once you've add enough to your commit (you only need to add the files you've changed), you can now 'commit' (think making a list of all the changes you want to make to your library book).
    
            git commit -m 'type a message here briefly describing the changes in this commit'
            
    - Once you've made the commits you want to (you can make more than one) you can now 'push' these commits to Github (think submitting the list of changes you made in your library book back to the library (or publisher)) You've now backed up your changes on Github, so keep working or move on to the next step.
    
            git push origin <branch_name>

    - Now, go to the website of your Github repo and look at the branches tab for the branch you just pushed, click on the button that says 'New pull request and merge'. Click 'Create pull request'. Github will check to see if you've done anything wrong and then let you confirm the request (if you have permission), do so. Now you've created a pull request and merged your newly edited branch with the master (the publish accepted your changes and published a revised version of the book.
    - Go back to your local machine and get the new version by pulling (checkout the master branch).

            git pull 
            
    - Here, good practice would be to delete the branch you just merged on Github and also locally (you'll need to be in a different branch, like master, to do this).

            git branch -d <branch_name>
            
    - You can now start the cycle over by creating a new branch to edit.