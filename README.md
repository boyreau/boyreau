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
	playbook_fb7ee37c("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_1290e5c2["play #1 (Get init process name): 4"]
		style play_1290e5c2 stroke:#c20a2a,fill:#c20a2a,color:#ffffff
		playbook_fb7ee37c --> |"1"| play_1290e5c2
		linkStyle 0 stroke:#c20a2a,color:#c20a2a
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_3d0f3d7e["play #2 (Gitea personnal instance): 1"]
		style play_3d0f3d7e stroke:#7e2d9f,fill:#7e2d9f,color:#ffffff
		playbook_fb7ee37c --> |"2"| play_3d0f3d7e
		linkStyle 1 stroke:#7e2d9f,color:#7e2d9f
			%% Start of the role '[role] gitea'
			play_3d0f3d7e --> |"1 "| role_404d8218
			linkStyle 2 stroke:#7e2d9f,color:#7e2d9f
			role_404d8218(["[role] gitea"])
			style role_404d8218 fill:#7e2d9f,color:#ffffff,stroke:#7e2d9f
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_3bc02ffb["play #3 (Gitea action runner): 1"]
		style play_3bc02ffb stroke:#1ca9b0,fill:#1ca9b0,color:#ffffff
		playbook_fb7ee37c --> |"3"| play_3bc02ffb
		linkStyle 3 stroke:#1ca9b0,color:#1ca9b0
			%% Start of the role '[role] go'
			play_3bc02ffb --> |"1 "| role_afcea1f4
			linkStyle 4 stroke:#1ca9b0,color:#1ca9b0
			role_afcea1f4(["[role] go"])
			style role_afcea1f4 fill:#1ca9b0,color:#ffffff,stroke:#1ca9b0
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_3bc02ffb --> |"2 "| role_2dd85980
			linkStyle 5 stroke:#1ca9b0,color:#1ca9b0
			role_2dd85980(["[role] act_runner"])
			style role_2dd85980 fill:#1ca9b0,color:#ffffff,stroke:#1ca9b0
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
	%% End of the playbook './playbook.yaml'

```
