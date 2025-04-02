
1. git install
2. global configration
3. create a project folder
4. command -> git init  => empty gir ropp create
5. open in vs using code . in terminal


# file in vs 
    U => untracted/ working area
    A => Added / staging area
    M => Modified

# terms of area
1. working => git init  => the area where we write code
2. staging => git add file1.txt  => add to staging area => stores in caches memory
3. De-staging => git rm --cached file_name => remove from staging area and add to  untracted area
4. commit => git commit -m "message" => heap memory (m => message)

# first commit is root commit

    master -------------()---------
                         |
                         |
                         |
                         |
                         | commit



    1. who => name and email
    2. when  => date and time
    3. commit_id  => commit hash (40 alpha numeric character)
    4. commit msg => first commit message 

# command 
 1 => git init  //-> .git file will be created  / it working area 
 1 => rd /s /q .git
   -> rd: removes directory (command for deleting folders)
   -> /s: Deletes the .git folder and all its subdirectories
   -> /q: Deletes the folder quietly (without asking for confirmation).
   -> .git: The hidden folder that stores all Git history and configuration.
    
 2 => git add fielName //-> file add to stagging area / cached memory
 3 => git rm --cached fileName //-> remove for cached memory to working area
      git rm -r --cached . // -> remove all 
 4 => git reset --soft Head~1  //-> take back latest commit to stagging area
 5 => git reset --mixed Head~2 //-> take back latest commit to working area
 6 => git reset --hard Head~3  // naver use this command. before using this note hash id
 7 => git reset hard "hashId" // back to recet deleted head

# how to edit file ? 
10 git commit --amend -m "new message" // it allows you change in seme commit
11 git commit --amend --no-edit // when you want to use same commit in same message

# how to check number of commits in a branch 
11. git log // all information
12. git log --oneline // show all coomit in a single line information
13. ESC:WQ ==>TO eacapre or get out of the log or close vim editor

# Branching
master branch -> main branch
slave branch -> development branch

# how to rename master branch
14. git branch -m "branch name (always use small letter) "
15. git branch -M "brach name" // to change branch name forcefully


Prod (production) (current or latest version)

Pre-Prod (Testing)

Main/Master (development)

# why we use branches 
16. git branch branchName   (like featuer123/navbar)

# how to check branch is crated or not
17. git branch

# to move from one branch to ohter branch
18. git switch branchName
18. get checkout branchName

# to merge a branch
19. git merge branchName

# how to delete a branch
20. git branch -d branchName    

# types of merging a branch
a. fast forward merge
b. three merge 
c. reb ase merge
d. squashing merge

# fast forward merge
    git mearge brnachName
# three way mearse 
// current changes
// incomming changes

# git checkout -b branchName

# git show command 
1. git show // it show all commits
2. git

# force fully pull
 git pull origin master => normal pull
 git pull origin master --allow-unrelated-histories => forcefully pull

# SSH (Secure Shell)
it is cryptographic netwokr protocol used to securely authenicate nad connect to git repository. 
it allow you to interact with services like GitHub, GitLab, Bitbucked whithout entering you password and username each time.
-> Authentication: it uses public-key ctyptogaphy instead to password.
-> Convenience: no need to enter credential repeatedly.
-> Faster communication: more efficent than HTTP.
-> Automation: useful for script and CI/CD pipeline.
# How it works
-> you generate an SSH key pair(public or privet).
-> you add public key to to your git service.
-> you use privet key to authenticate when clonig, pusing and pulling.
# How to setup SSH for Git?
=> ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
-> ssh-keygen : command to generate key
-> -t rsa : Specifies RSA type key
-> -b 4096 : Sets 409 
-> -C : Add comments to you 