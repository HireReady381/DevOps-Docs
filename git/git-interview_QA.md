1. **Scenario 1: Undoing a Pushed Commit Without Affecting Other Users' History**
    
    You pushed a faulty commit to a shared branch. How can you fix the mistake without rewriting history?
    
    - Use `git revert` to create a new commit that negates the previous one.
    - **Example**:
        
        ```bash
        
        git revert <commit-hash>
        git push origin main
        
        ```
        
    - `git revert` creates a new commit that undoes the changes of the specified commit. This approach is safe for shared branches because it preserves the history.

---

**Scenario 2: Accidental Deletion of a Branch**

- You accidentally deleted a local branch. How do you recover it?
- If the branch has been pushed to the remote, you can fetch it. If not, find the commit hash in the reflog and recreate it.
- **Example**:
    
    ```bash
    
    git reflog
    git checkout -b recovered-branch <commit-hash>
    
    ```
    

---

**Scenario 3: Resolving a Conflict While Rebasing**

- During a rebase, you encounter conflicts. How do you resolve them and continue the rebase?
- 
    
    ```bash
    
    git status  # Shows conflicting files
    git add resolved-file.txt
    git rebase --continue
    
    ```
    

---

**Scenario 4: Squashing Commits in a Feature Branch**

- How would you squash multiple commits in a feature branch into a single commit before merging to `main`?
- Use interactive rebase:
    
    ```bash
    
    git checkout feature-branch
    git rebase -i main
    
    ```
    
- Mark commits as `squash` or `s` except for the first one.

---

**Scenario 5: Fixing a Commit Message After Pushing**

- How can you correct a commit message that was already pushed to the remote branch?
- 
    
    ```bash
    
    git commit --amend -m "Correct message"
    git push --force
    
    ```
    

---
