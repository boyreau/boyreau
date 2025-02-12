<h2 align="left">Hi 👋! My name is Arthur and I'm a DevOps, from France</h2>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=boyreau&hide_title=false&hide_rank=true&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=boyreau&locale=en&hide_title=false&count_private=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>

###

<img align="right" height="150" src="https://i.imgflip.com/1o3xse.jpg"  />

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" height="30" alt="Docker logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ansible/ansible-original.svg" height="30" alt="Ansible logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="30" alt="Git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/githubactions/githubactions-original.svg" height="30" alt="GitHub Actions logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg" height="30" alt="Django logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" height="30" alt="Bash logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="30" alt="C logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/archlinux/archlinux-original.svg" height="30" alt="Arch Linux logo"  />
  <img width="12" />
</div>

###

<div align="left">
  <img src="https://img.shields.io/static/v1?message=Codeberg&logo=codeberg&label=&color=4793CC&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="codeberg logo"  />
  <img src="https://img.shields.io/static/v1?message=ProtonMail&logo=protonmail&label=&color=6D4AFF&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="proton mail logo"  />
  <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo"  />
</div>

###

<br clear="both">

###
```mermaid
---
title: "My super-well-designed Ansible mess"
---
%%{ init: { "flowchart": { "curve": "bumpX" } } }%%
flowchart LR
	%% Start of the playbook './playbook.yaml'
	playbook_463af9b1("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_8c975b44["play #1 (Get init process name): 4"]
		style play_8c975b44 stroke:#704884,fill:#704884,color:#ffffff
		playbook_463af9b1 --> |"1"| play_8c975b44
		linkStyle 0 stroke:#704884,color:#704884
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_f46c0331["play #2 (Gitea personnal instance): 1"]
		style play_f46c0331 stroke:#873d8f,fill:#873d8f,color:#ffffff
		playbook_463af9b1 --> |"2"| play_f46c0331
		linkStyle 1 stroke:#873d8f,color:#873d8f
			%% Start of the role '[role] gitea'
			play_f46c0331 --> |"1 "| role_3863489f
			linkStyle 2 stroke:#873d8f,color:#873d8f
			role_3863489f(["[role] gitea"])
			style role_3863489f fill:#873d8f,color:#ffffff,stroke:#873d8f
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_9eb101d9["play #3 (Gitea action runner): 1"]
		style play_9eb101d9 stroke:#627b51,fill:#627b51,color:#ffffff
		playbook_463af9b1 --> |"3"| play_9eb101d9
		linkStyle 3 stroke:#627b51,color:#627b51
			%% Start of the role '[role] go'
			play_9eb101d9 --> |"1 "| role_d705e651
			linkStyle 4 stroke:#627b51,color:#627b51
			role_d705e651(["[role] go"])
			style role_d705e651 fill:#627b51,color:#ffffff,stroke:#627b51
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_9eb101d9 --> |"2 "| role_9b432777
			linkStyle 5 stroke:#627b51,color:#627b51
			role_9b432777(["[role] act_runner"])
			style role_9b432777 fill:#627b51,color:#ffffff,stroke:#627b51
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
	%% End of the playbook './playbook.yaml'

```
