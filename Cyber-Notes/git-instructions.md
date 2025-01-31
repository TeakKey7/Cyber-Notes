# Obsidian instructions

## Downloading the repository
1. If you want permissions to create a branch, please chat me on Discord @TeakKey7
2. Once you have permissions to edit (or if you only care to view directly), go to the [Github repo](https://github.com/TeakKey7/Cyber-Notes) and click the green `Code` button from here you have two choices
	1. [Https setup](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#https) (Use personal access token as password)
	2. [SSH setup](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#ssh)
3. Now ensure you have [git](https://git-scm.com/downloads) installed.
4. cd to the correct folder. Note it will clone into a subfolder. If your working directory is `~/obsidian` the repository will land on `~/obsidian/Cyber-Notes` 
5. Run `git clone git@github.com:TeakKey7/Cyber-Notes.git` for SSH or `git clone https://github.com/TeakKey7/Cyber-Notes.git` for HTTPS
> Note: The Obsidian vault is `Cyber-Notes/Cyber-Notes` not the root of the repo
## Loading the Obsidian Vault
6. Go to the [Github repo](https://github.com/TeakKey7/Cyber-Notes) and clone it to a folder. Follow instructions if necessary
7. You should receive a folder containg `Cyber-Notes`
	1. The second folder is where you are going to point an [Obsidian]() vault import. The root folder is for web hosting.
8. Make sure to accept plugin permissions
9. On the left bar you should see Source Control :material-source-pull: and command palette. :fontawesome-solid-terminal: You will need both for the next step. 
## Creating a branch to edit from
1. Open command palette :fontawesome-solid-terminal: on the left 
2. Type `git create new branch`
	1. Type your branches name
3. Open source control :material-source-pull:
	1. A new panel should appear on the right 
	2. Push (:octicons-upload-16:)
	3. Select origin
	4. Type `origin/[BRANCH]` 
4. Done.