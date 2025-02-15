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
	playbook_9fd6921e("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_43e08b53["play #1 (Get init process name): 4"]
		style play_43e08b53 stroke:#6e2aa2,fill:#6e2aa2,color:#ffffff
		playbook_9fd6921e --> |"1"| play_43e08b53
		linkStyle 0 stroke:#6e2aa2,color:#6e2aa2
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_6d4593f7["play #2 (Gitea personnal instance): 1"]
		style play_6d4593f7 stroke:#2483a8,fill:#2483a8,color:#ffffff
		playbook_9fd6921e --> |"2"| play_6d4593f7
		linkStyle 1 stroke:#2483a8,color:#2483a8
			%% Start of the role '[role] gitea'
			play_6d4593f7 --> |"1 "| role_552bcdb0
			linkStyle 2 stroke:#2483a8,color:#2483a8
			role_552bcdb0(["[role] gitea"])
			style role_552bcdb0 fill:#2483a8,color:#ffffff,stroke:#2483a8
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_a615e5ae["play #3 (Gitea action runner): 1"]
		style play_a615e5ae stroke:#cc7700,fill:#cc7700,color:#ffffff
		playbook_9fd6921e --> |"3"| play_a615e5ae
		linkStyle 3 stroke:#cc7700,color:#cc7700
			%% Start of the role '[role] go'
			play_a615e5ae --> |"1 "| role_466a7b4d
			linkStyle 4 stroke:#cc7700,color:#cc7700
			role_466a7b4d(["[role] go"])
			style role_466a7b4d fill:#cc7700,color:#ffffff,stroke:#cc7700
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_a615e5ae --> |"2 "| role_8f6f9f57
			linkStyle 5 stroke:#cc7700,color:#cc7700
			role_8f6f9f57(["[role] act_runner"])
			style role_8f6f9f57 fill:#cc7700,color:#ffffff,stroke:#cc7700
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
	%% End of the playbook './playbook.yaml'

```
