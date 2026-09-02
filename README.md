# Welcome to our AI Bootcamp repository! 

## Start Here

If you are setting up Git for the first time, please authenticate your machine and configure your identity so GitHub recognizes it. 

#### 1. Setup via Terminal (Command Line)
Follow the official steps on the [GitHub Git Setup Guide](https://docs.github.com/en/get-started/git-basics/set-up-git#setting-up-git) to download Git and authenticate. 

#### 2. Next, clone this repo
Pre-req: Git should be installed on your machine.

1. **Open up a terminal on you laptop.**
1. **Clone this repository locally:** `git clone <ORIGINAL_REPO_URL>`
2. **Navigate to that folder on your computer:** `cd <PATH_TO_CLONED_REPO>`
3. **Create new repo:** Go to GitHub and create a new, empty repository (do not add a README or license).
4. **Change tracking URL:** `git remote set-url origin <YOUR_NEW_GITHUB_URL>`
5. **Push everything:** `git push -u origin main`

#### 3. Setup your AI Coding Harness (GitHub Copilot App)
For an AI-native desktop environment, we will be using the standalone [GitHub Copilot App](https://github.com/features/ai/github-app). 
This app acts as a central control center for AI agents to run builds, test code, and manage repositories directly from the desktop without needing heavy terminal configuration.

* **To connect:** Download the app, open it, and log in with a GitHub account. It handles authorization automatically.
* **To add your new repo (the one you just pushed):** Click the **+** symbol inside the app interface, click **Github repository** paste that new GitHub URL. The AI can then read the codebase, track changes, and help write code directly through chat or agent mode.

#### 4. Lastly, get Visual Studio Code 
Install it from [here](https://code.visualstudio.com) and follow the on-screen instructions. Once it's installed, open up the local folder on your computer containing the new repository.
