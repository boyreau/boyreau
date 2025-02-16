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
	playbook_79ead005("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_6c311acf["play #1 (Get init process name): 4"]
		style play_6c311acf stroke:#8e603e,fill:#8e603e,color:#ffffff
		playbook_79ead005 --> |"1"| play_6c311acf
		linkStyle 0 stroke:#8e603e,color:#8e603e
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_8fe9a748["play #2 (Mysql gitea database): 1"]
		style play_8fe9a748 stroke:#3001cb,fill:#3001cb,color:#ffffff
		playbook_79ead005 --> |"2"| play_8fe9a748
		linkStyle 1 stroke:#3001cb,color:#3001cb
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_aa23e2e9["play #3 (Gitea action runner): 1"]
		style play_aa23e2e9 stroke:#30409c,fill:#30409c,color:#ffffff
		playbook_79ead005 --> |"3"| play_aa23e2e9
		linkStyle 2 stroke:#30409c,color:#30409c
			%% Start of the role '[role] go'
			play_aa23e2e9 --> |"1 "| role_0e88b7f5
			linkStyle 3 stroke:#30409c,color:#30409c
			role_0e88b7f5(["[role] go"])
			style role_0e88b7f5 fill:#30409c,color:#ffffff,stroke:#30409c
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_aa23e2e9 --> |"2 "| role_ee87e923
			linkStyle 4 stroke:#30409c,color:#30409c
			role_ee87e923(["[role] act_runner"])
			style role_ee87e923 fill:#30409c,color:#ffffff,stroke:#30409c
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
		%% Start of the play 'play #4 (Nginx reverse proxy): 1'
		play_6ef56bfe["play #4 (Nginx reverse proxy): 1"]
		style play_6ef56bfe stroke:#374395,fill:#374395,color:#ffffff
		playbook_79ead005 --> |"4"| play_6ef56bfe
		linkStyle 5 stroke:#374395,color:#374395
			%% Start of the role '[role] nginx-reverse-proxy'
			play_6ef56bfe --> |"1 "| role_7791370c
			linkStyle 6 stroke:#374395,color:#374395
			role_7791370c(["[role] nginx-reverse-proxy"])
			style role_7791370c fill:#374395,color:#ffffff,stroke:#374395
			%% End of the role '[role] nginx-reverse-proxy'
		%% End of the play 'play #4 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
