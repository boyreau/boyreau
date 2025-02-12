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
	playbook_fc16d71b("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_2345da04["play #1 (Get init process name): 4"]
		style play_2345da04 stroke:#4e9834,fill:#4e9834,color:#ffffff
		playbook_fc16d71b --> |"1"| play_2345da04
		linkStyle 0 stroke:#4e9834,color:#4e9834
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_89e2a681["play #2 (Gitea personnal instance): 1"]
		style play_89e2a681 stroke:#b61649,fill:#b61649,color:#ffffff
		playbook_fc16d71b --> |"2"| play_89e2a681
		linkStyle 1 stroke:#b61649,color:#b61649
			%% Start of the role '[role] gitea'
			play_89e2a681 --> |"1 "| role_7e1304d3
			linkStyle 2 stroke:#b61649,color:#b61649
			role_7e1304d3(["[role] gitea"])
			style role_7e1304d3 fill:#b61649,color:#ffffff,stroke:#b61649
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_d640eab3["play #3 (Gitea action runner): 1"]
		style play_d640eab3 stroke:#ab5121,fill:#ab5121,color:#ffffff
		playbook_fc16d71b --> |"3"| play_d640eab3
		linkStyle 3 stroke:#ab5121,color:#ab5121
			%% Start of the role '[role] go'
			play_d640eab3 --> |"1 "| role_8d25994f
			linkStyle 4 stroke:#ab5121,color:#ab5121
			role_8d25994f(["[role] go"])
			style role_8d25994f fill:#ab5121,color:#ffffff,stroke:#ab5121
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_d640eab3 --> |"2 "| role_af6c4d7f
			linkStyle 5 stroke:#ab5121,color:#ab5121
			role_af6c4d7f(["[role] act_runner"])
			style role_af6c4d7f fill:#ab5121,color:#ffffff,stroke:#ab5121
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
	%% End of the playbook './playbook.yaml'

```
