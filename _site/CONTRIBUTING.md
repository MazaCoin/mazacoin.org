# CONTRIBUTING

Contributors fork the main repo, and work in their own accounts, and
submit their work as a Pull Request.

## Guidelines

 - Technical informative pages are encouraged
 - Political and Commercial content discouraged, and unlikely to be merged
 - Listings of Exchanges, Wallets, Service Providers are accepted
    - criteria is not yet developed for inclusion in lists 
 - Static content only - html, markdown etc. (no Javascript, PHP, etc)

## Procedure 
### basic master-develop workflow
Following the general instructions found in Github's Tutorials
 - [here](https://help.github.com/articles/fork-a-repo/)
 - [here](https://help.github.com/articles/using-pull-requests/)

1. Fork mazacoin.org to your account
2. if needed, clone your newly forked repo to your local machine
3. checkout develop branch
  ```
  git checkout develop
  ```
4. now checkout a new branch based on develop
  ```
  git checkout -b my-new-kewl-stuffs
  ```
5. make needed changes
6. add your changes
  ```
  git status 
  git add <file> <file> OR git add --all 
  ```
7. Commit and Push your changes to your repo
  git commit -m "Did something to something"
  git push origin my-new-kewl-stuffs
  ```
8. Return to your repo on github web,
   You should now see a button to create a Pull Request
   Ensure that the Base is mazacoin/mazacoin.org:develop
   Click to start PR
9. Once 2 or more committers have agreed (ideally 3 or more) 
   by form of commenting "ACK" "untestedACK" PR may be merged to develop branch.
10. [ NEED AUTOMATION ]
    - currently develop can be merged to gh-pages 
    - github will display gh-pages branch [here](https://mazacoin.github.io/mazacoin.org/)
    - committers & reviewers may then check above site
11. PR develop to master
    - NEED AUTOMATION (website currently pulls master 30min intervals)
    
