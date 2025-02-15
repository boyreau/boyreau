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
	playbook_58771bd0("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_516c29f7["play #1 (Get init process name): 4"]
		style play_516c29f7 stroke:#a22a83,fill:#a22a83,color:#ffffff
		playbook_58771bd0 --> |"1"| play_516c29f7
		linkStyle 0 stroke:#a22a83,color:#a22a83
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_67f67a36["play #2 (Gitea personnal instance): 1"]
		style play_67f67a36 stroke:#0bc13b,fill:#0bc13b,color:#ffffff
		playbook_58771bd0 --> |"2"| play_67f67a36
		linkStyle 1 stroke:#0bc13b,color:#0bc13b
			%% Start of the role '[role] gitea'
			play_67f67a36 --> |"1 "| role_1f3d9f96
			linkStyle 2 stroke:#0bc13b,color:#0bc13b
			role_1f3d9f96(["[role] gitea"])
			style role_1f3d9f96 fill:#0bc13b,color:#ffffff,stroke:#0bc13b
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_c1192f12["play #3 (Gitea action runner): 1"]
		style play_c1192f12 stroke:#4e0fbd,fill:#4e0fbd,color:#ffffff
		playbook_58771bd0 --> |"3"| play_c1192f12
		linkStyle 3 stroke:#4e0fbd,color:#4e0fbd
			%% Start of the role '[role] go'
			play_c1192f12 --> |"1 "| role_fc9e2cc2
			linkStyle 4 stroke:#4e0fbd,color:#4e0fbd
			role_fc9e2cc2(["[role] go"])
			style role_fc9e2cc2 fill:#4e0fbd,color:#ffffff,stroke:#4e0fbd
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_c1192f12 --> |"2 "| role_c15c38af
			linkStyle 5 stroke:#4e0fbd,color:#4e0fbd
			role_c15c38af(["[role] act_runner"])
			style role_c15c38af fill:#4e0fbd,color:#ffffff,stroke:#4e0fbd
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
	%% End of the playbook './playbook.yaml'

```
