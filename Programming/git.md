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


# Using WebLatex
Important:  
1. Create Codespace
2. Write your latex, generate pdf
3. Use command line to pull, push commit!
4. Turn off Codespace!

Viewing codespace usage  
https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-github-codespaces/viewing-your-github-codespaces-usage  

Turn off codespace when done using it!!! Don't waste core time!  
https://github.com/orgs/community/discussions/17019  

Don't delete your codespace yet!  
https://docs.github.com/en/codespaces/developing-in-a-codespace/deleting-a-codespace  

Codespace taking forever to commit? Don't forget to write commit message!  
https://stackoverflow.com/questions/75244108/why-is-the-commit-operation-taking-forever-in-visual-studio-code

# Q&A
How to add all modified files  
https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add

How to delete git repo  
https://stackoverflow.com/questions/1213430/how-to-fully-delete-a-git-repository-created-with-init

How to download whole repository without turning it into git  
https://stackoverflow.com/questions/57048400/how-do-i-convert-a-git-repository-folder-into-a-regular-folder  
https://stackoverflow.com/questions/160608/do-a-git-export-like-svn-export

# References
Nice quickstart example  
https://docs.github.com/en/get-started/using-git/about-git

Git tutorial  
https://git-scm.com/docs/gittutorial

git commit  
https://git-scm.com/docs/git-commit#_options

