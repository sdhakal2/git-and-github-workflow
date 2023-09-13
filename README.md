# Git and Github Workflow

A comprehensive Git and Github workflow while multiple developers are working on the same project. 

1. **Setup or update:** Clone a repo from Github or update to the latest changes. 
   
   ```bash
   #Using Git may require authenticating every time. 
   git clone <repo> 
   #Using the Github command line tool. gh can be authenticated just onee. 
   gh repo clone <project_path_from_Github> 
   #--OR--
   #Checkout the main branch.
   git checkout main
   #Pull the latest changes.
   git pull origin main
   ```

2. **Create a new branch:** Create a new branch implementing required changes.
   
   ```bash
   #Create and checkout a new branch.
   git checkout -b <new_branch_name> # for instance feature/add-product-class
   ```

3. **Work on the change:** Implement the required changes and commit the changes.
   
   ```bash
   #Stage all changes.
   git add . 
   #Commit changes.
   git commit -m "<commit message in simple present tense>"
   ```

4. **Regularly pull latest changes from the main:** Regularly update the new branch by pulling changes from the main or master branch while working on the current changes.
   
   ```bash
   #Checkout the new branch.
   git checkout <new_branch_name>
   #Pull changes from the main. 
   git pull origin main
   ```
   
5. **Resolve conflict (if necessary):** Resolve conflict between the main and the new branch if necessary. 
   
6. **Pull request:** Open a new pull request in Github.
   * Go to repository on GitHub.
   * Click the "New Pull Request" button.
   * Select the main branch as the base branch and the new branch as the compare branch.
   * Write a descriptive title and detailed description for the pull request.
   * Request a code reviews.
  
7. **Review and merge changes:** Review the new changes and merge them with main or master branch on Github. 
   
8. **Update the local main:** Once review and merge complete on Github, update the local repo's main or master branch. 
   
   ```bash
   #Checkout the main or master branch.
   git checkout main
   #Update the change from Github. 
   git pull origin main
   ```

9.  **Repeat step 2-8:** Repeat this process of checkout, pull request, merge, and update for all changes. 

10. **Delete the new branch (optional):** Delete the new branch if no longer needed.
    ```bash
    #Delete locally.
    git branch -d <new_branch_name>
    #Delete on Github.
    git delete push origin --delete <new_branch_name>
    ```