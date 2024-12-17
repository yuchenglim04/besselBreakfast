# First time
    git clone https://github.com/yuchenglim04/besselBreakfast     #creates a folder.
    git push --set-upstream origin <branchname>                 #merge with online repo; branchname might be main
    
# Subsequent
    git pull                                            #update local repo to match online repo
    git push                                            #merge; always pull before you push

# General
    git status                                              #can check branch
    git commit -m "message"
    git add <filename>                                  #to make git aware of the file
    git add .

# Resolve diverging branches
    git merge origin/main -m "message"                          #origin means the one online, like git pull, but works for diverging branches


# Frequent sequence of commands:
        git pull
        <modify file>
        git add .
        git status
        git commit -m "message"
        git push

# To delete a local git repo
        ls -al            # to reveal .git directory in your repo
        rm -rf .git       
        rm <repo name>


# References
Nice quickstart example  
https://docs.github.com/en/get-started/using-git/about-git

Git tutorial  
https://git-scm.com/docs/gittutorial

How to add all modified files  
https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add

How to delete git repo  
https://stackoverflow.com/questions/1213430/how-to-fully-delete-a-git-repository-created-with-init

git commit  
https://git-scm.com/docs/git-commit#_options
