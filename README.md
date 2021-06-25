# Welcome to CleanCodeWorkshop :checkered_flag:

<span style="width:100%">[![forthebadge](https://forthebadge.com/images/badges/built-by-developers.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/powered-by-coffee.svg)](https://forthebadge.com)
</span>



<span style="width:100%">[![forthebadge](https://forthebadge.com/images/badges/0-percent-optimized.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/powered-by-responsibility.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/uses-badges.svg)](https://forthebadge.com)
</span>


<img align=right width="30%" height="40%" src="https://i.makeagif.com/media/7-20-2017/tglPfl.gif" />

## About the Workshop 

* This workshop is conducted for the hands-on learning of the best Clean Coding practices.

## Agenda of the Workshop 
	
* overview and explanation
* break
* practical via gitlab code in small groups
* coming back to discuss learnings.

<img align='bottom' width="100%" height="100%" src="https://www.cleancodefactory.de/Content/Images/Factory_slow.gif" />


## Rules :boom:

<img align=right width="35%" height="200px" src="https://i.imgur.com/rfELtKE.gif"/>

### 1) Fork this repo incase facing issue follow this documentation.
### 2) Every member is assigned to a group.
### 4) There are branches based on group name. Refactor the code. 
### 5) Create a PR [ Pull Request ] for that particular branch only.
### 6) There are multiple levels in which questions are designed.


<!-- <img align='bottom' width="30%" height="40%" src="https://i.pinimg.com/originals/f4/ed/d7/f4edd74d05ab9268f021a6a0ada5cd2e.gif" /> -->
<!-- <img align='bottom' width="30%" height="40%" src="https://milanlatinovic.com/wp-content/uploads/2019/03/clean-code-rules.gif" /> -->
<!-- <img align='bottom' width="30%" height="40%" src="https://i.giphy.com/media/ef7GqsDYDIKFa/giphy.gif" /> -->

## Github CLI 

Installing gh cli [link](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)

```bash 

curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo gpg --dearmor -o /usr/share/keyrings/githubcli-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null

sudo apt update

sudo apt install gh

gh auth login
```
![GH Install Gif](gifs/installGH.gif)
![GH done](gifs/gh_setup_done.png)

```bash
# Clone the repo 
git clone https://github.com/Imsurajkr/cleancodeworkshop.git
cd cleancodeworkshop
gh repo fork 
parentBranch=GroupName # Replace Group Name with your group 
candidateName=MemberName # Replace MemberName with your Name
branchName="$parentBranch-$candidateName"
git checkout -b $branchName
# Add Your magic When done 
git pull 
git add <FilesChanged> 
git commit -m "Customized Message"
git push 
gh pr create --title "I did some changes" --body "And it works"
# All the best :-)
```
![GH Install Gif](gifs/forkGH.gif)
![PR Raised](gifs/pr_created.png)