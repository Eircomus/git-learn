# git-learn
learning how git and github work 

The workflow should look like this:

0. Sign up for a Github account & Install Git on Your Computer(Linux/Mac/Windows etc.)

1. Set Up Git Locally
    git config --global user.name "YourGitHubUsername"
    git config --global user.email "your-email@example.com"

2. Create a New Repository on GitHub

3. Initialize Git in Your Project Folder
    cd /path/to/your/project  # Navigate to your project folder
    git init  # Initialize Git in the folder

4. Link Your Local Project to GitHub
    git remote add origin https://github.com/Username/my-project.git

5. Add and Commit Your Files
    git add filename
    git commit -m "Initial commit"

6. Push Your Code to GitHub
    git branch -M main  # Rename default branch to 'main'
    git push -u origin main  # Push code to GitHub

7. Keep Updating Your Project
    git add filename
    git commit -m "Updated some features"
    git push origin main


<Important!> Use SSH Authentication

If you don't want to enter credentials every time, you can set up SSH authentication.

1. Check if you already have SSH keys
    ls -al ~/.ssh

2. Generate a new SSH key
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ssh-add ~/.ssh/id_ed25519 # Add your SSH private key to the ssh-agent.

3. Add the SSH key to GitHub
    cat ~/.ssh/id_ed25519.pub # Copy the output. Go to GitHub SSH Settings. Click "New SSH Key", paste the key, and save.

4. Test SSH connection
    ssh -T git@github.com # success message: Hi GITHUB_USERNAME! You've successfully authenticated, but GitHub does not provide shell access.

5. Change your Git remote URL to use SSH
    git remote set-url origin git@github.com:Username/your-project.git

6. Now push without needing a password
    git push origin main or git push -u origin main (to set upstream if pushing for the first time)

That's it! SSH authentication is now set up. You won’t need to enter a username or password anymore! 🎉



