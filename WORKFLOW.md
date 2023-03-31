# Setting up the environment

## VS Code with auto formatting (JavaScript and Solidity)

1. Install VS Code from here: https://code.visualstudio.com/
1. On VS Code, install the extensions **Solidity + Hardhat** and **Prettier**
1. **Ctrl + Shift + P**, then `Preferences: Open User Settings (JSON)`
1. Add the lines: `"editor.formatOnSave": true, "[solidity]": { "editor.defaultFormatter": "NomicFoundation.hardhat-solidity" }, "[javascript]": { "editor.defaultFormatter": "esbenp.prettier-vscode" },`

## Install Node Js

1. Install Node Version Manager by opening a terminal and running `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`
2. **Close the terminal**, then open a new one, and run `nvm --version` to see if Node Version Manager actually installed.
3. Run `nvm install 16.14.2` to install Node Js.
4. Run `node --version` to see if Node Js installed.

### Enable Yarn (Node Js required)

1. Run `corepack enable`. If it's not available, run `npm i -g corepack` first.
2. Check if it's installed with `yarn --version`

## Enable hh shorthand

`npm install --global hardhat-shorthand` to use commands like `hh compile` instead of `yarn hardhat compile`

## Windows only (to get the Linux console)

### Install WSL (Windows Subsystem for Linux)

1. Type `powershell` on Start Menu, right-click, "Run as Administrator", then run `wsl --install`.
2. Restart computer after installation completes.
3. Set user and password for your Ubuntu installation after you restart. If it doesn't prompt automatically after restart, type `ubuntu` on Start Menu and run it.
4. Open VS Code and install the extension **Remote Development**

### Run WSL

- On VS Code, press **Ctrl + Shift + P**, type `wsl` then click **Remote-WSL: New WSL Window** to open a Linux terminal.
- Type `ubuntu` on Start Menu, run it, then type `mkdir FOLDER_NAME` to create a new folder, `cd FOLDER_NAME` to move into that folder, and `code .` to run VS Code from that folder.

### Install Git on WSL

1. Check if it's already installed with `git --version`
2. If not, install Git following the instructions for Linux here https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

# Upload project to GitHub

1. Do NOT forget to create a `.gitignore` file and list there all files containing sensitive data, like `.env`. Also, list all the unnecesary files that you can download with `yarn` or `yarn hardhat compile`.

It may look like this:
`node_modules .env artifacts cache ...`

2. Initialize git on the root directory with `git init`

3. Create a new repository on github and run the command `git remote add origin (YOUR_REPO_URL)`

4. Change the branch to main with `git branch -M main`
   (git uses "master" as default, mmm yeah Mommy ;) )

5. Stage and commit the files for your first commit with `git add .` then `git commit -m "First commit"`

6. Push them to GitHub with `git push -u origin main`