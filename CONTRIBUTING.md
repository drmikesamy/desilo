# Contributing to Desilo - A guide for complete beginners

## The Easy Way - Directly Editing in GitHub

### Step 1: Create a GitHub Account
- If you don't already have an account, go to [GitHub](https://github.com) and sign up.

### Step 2: Fork the Desilo Repository
- Go to the repository page you want to contribute to. For the Desilo repository, [click here](https://github.com/drmikesamy/desilo).  
- Click the **"Fork" button** in the top-right corner to create your own personal copy of the repository in your account.

### Step 3: Edit Files
- Click your username at the top-left of the page to see your repositories.  
- Select the forked Desilo repository and navigate to the file you want to edit.  
- Click the **pencil icon** (at the top-right of the file view) to edit the file directly in your browser. You can switch between Edit and Preview modes at the top of the editing area to see how your changes look.

### Step 4: Commit Changes
- After editing, scroll to the "Commit changes" green button near the top right of the page.  
- Add a descriptive commit message and click the **"Commit changes"** button.

### Step 5: Create a Pull Request (PR)
- Go back to the original repository.  
- Click the **"Pull Requests" tab** and then click **"New Pull Request"**.  
- Select your forked repository and branch as the source, and the original repository and branch as the target.  
- Add a title and description for your PR, then click **"Create Pull Request"**.
- The maintainers of Desilo will review your proposed Pull Request, test if necesssary, and merge your changes into the main Desilo project if approved.


## The Right Way - Clone to your Local Machine

### Step 1: Create a GitHub account

### Step 2: Fork the Desilo Repository
1. **Go to the repository page** on GitHub. For the Desilo repository page, [click here](https://github.com/drmikesamy/desilo)
2. Click the **"Fork" button** in the top-right corner. This will create a copy of the repository under your own GitHub account.

### Step 3: Clone the Forked Repository to your local computer
1. When you click your username at the top left of the page, you will see a list of your repositories, including the Desilo repository that is a copy of the main repository. Think of this as your very own version of the whole Desilo documentation and codebase you can freely edit without external permissions. Click the Desilo repository to go into it. On your Desilo repository page, click the green **"Code" button**.
2. Copy the URL in the dropdown box (HTTPS). It should look like this: https://github.com/{your GitHub username}/desilo.git
3. Open your terminal (e.g. Windows Powershell or Terminal on Mac/Linux), navigate to the folder you want to download the repository to, with a command like this (in this case it will go to your user/home directory):
   ```bash
   cd ~
   ```
4. ...and run this, replacing {your GitHub username} with your GitHub username:
   ```bash
   git clone https://github.com/{your GitHub username}/desilo.git
   ```
5. Now you should see the folder in your home directory.
### Step 4: Open the Repository on your local computer
1. Download Visual Studio Code here, and install it on your computer: (https://code.visualstudio.com). Open it and go to File -> Open Folder. Choose the folder you just cloned.
2. Click the icon on the top left of Visual Studio code, that looks like two stacked sheets of paper. You will see all the files and folders of the repository.
3. Edit files. You can add your general ideas and modifications in README.md, or edit the technical design of the protocol in DIPs/DIP01.md etc.
### Step 5: Push your changes to your personal Desilo repository on GitHub
1. In Visual Studio Code, click the third icon down in the left hand side menu, the one that looks like a tube map. This is the Git section.
2. Click the Sign In button and sign in with your GitHub details.
3. In the Message text box, type a short description of what you changed.
4. Click Commit and then click Sync Changes.
5. You can now follow step 5 of The Easy Way guide above.
