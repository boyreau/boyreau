<h2 align="left">Hi 👋! My name is Arthur and I'm a DevOps, from France</h2>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=boyreau&hide_title=false&hide_rank=true&show_icons=true&include_all_commits=true&count_private=false&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
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
	playbook_827e3f67("./playbook.yaml")
		%% Start of the play 'play #1 (Gitea personnal instance): 1'
		play_aa334636["play #1 (Gitea personnal instance): 1"]
		style play_aa334636 stroke:#13b98e,fill:#13b98e,color:#ffffff
		playbook_827e3f67 --> |"1"| play_aa334636
		linkStyle 0 stroke:#13b98e,color:#13b98e
			%% Start of the role '[role] gitea'
			play_aa334636 --> |"1 "| role_e0f7329d
			linkStyle 1 stroke:#13b98e,color:#13b98e
			role_e0f7329d(["[role] gitea"])
			style role_e0f7329d fill:#13b98e,color:#ffffff,stroke:#13b98e
			%% End of the role '[role] gitea'
		%% End of the play 'play #1 (Gitea personnal instance): 1'
	%% End of the playbook './playbook.yaml'

```
