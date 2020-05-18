# Gitting started.
Welcome to the Luger Lab! This repository (or repo) will introduce you into the organizaton and usage of this Github page.

## Navigation.
This Github page is organized into repos of scripts relating to different projects in the lab. If you are looking for a piece of software first look for the related repo, then read through the README file for more information.

### LugerLab repos are composed of the following:
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

## Using Luger Lab software.
1. **Cloning** In order to use software from Github you need to 'clone' the repo (aka copy the folder containing the program). 

## Contributing.            
1. There are two main ways to start a new repo:
    - The easiest way is to simply use the 'New' button on the LugerLab mainpage, create the repo, and clone it into the loaction of your choosing on your local computer.
    - Conversely, you can navigate into a folder and use 
    ...
    git init
    git remote add origin git@github.com:username/new_repo
    git push -u origin master
    ...
2. Either way you've chosen to start a repo you will need to add 