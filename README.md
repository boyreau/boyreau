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
	playbook_6df43d61("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_84b6ed82["play #1 (Get init process name): 4"]
		style play_84b6ed82 stroke:#2f9d90,fill:#2f9d90,color:#ffffff
		playbook_6df43d61 --> |"1"| play_84b6ed82
		linkStyle 0 stroke:#2f9d90,color:#2f9d90
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_6b9627e2["play #2 (Gitea personnal instance): 1"]
		style play_6b9627e2 stroke:#a82a24,fill:#a82a24,color:#ffffff
		playbook_6df43d61 --> |"2"| play_6b9627e2
		linkStyle 1 stroke:#a82a24,color:#a82a24
			%% Start of the role '[role] gitea'
			play_6b9627e2 --> |"1 "| role_7ee01add
			linkStyle 2 stroke:#a82a24,color:#a82a24
			role_7ee01add(["[role] gitea"])
			style role_7ee01add fill:#a82a24,color:#ffffff,stroke:#a82a24
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_31972b10["play #3 (Gitea action runner): 1"]
		style play_31972b10 stroke:#5007c5,fill:#5007c5,color:#ffffff
		playbook_6df43d61 --> |"3"| play_31972b10
		linkStyle 3 stroke:#5007c5,color:#5007c5
			%% Start of the role '[role] go'
			play_31972b10 --> |"1 "| role_30f31cc9
			linkStyle 4 stroke:#5007c5,color:#5007c5
			role_30f31cc9(["[role] go"])
			style role_30f31cc9 fill:#5007c5,color:#ffffff,stroke:#5007c5
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_31972b10 --> |"2 "| role_a063e626
			linkStyle 5 stroke:#5007c5,color:#5007c5
			role_a063e626(["[role] act_runner"])
			style role_a063e626 fill:#5007c5,color:#ffffff,stroke:#5007c5
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
		%% Start of the play 'play #4 (Nginx reverse proxy): 1'
		play_6c3236cc["play #4 (Nginx reverse proxy): 1"]
		style play_6c3236cc stroke:#b41834,fill:#b41834,color:#ffffff
		playbook_6df43d61 --> |"4"| play_6c3236cc
		linkStyle 6 stroke:#b41834,color:#b41834
			%% Start of the role '[role] nginx-reverse-proxy'
			play_6c3236cc --> |"1 "| role_31d7e87b
			linkStyle 7 stroke:#b41834,color:#b41834
			role_31d7e87b(["[role] nginx-reverse-proxy"])
			style role_31d7e87b fill:#b41834,color:#ffffff,stroke:#b41834
			%% End of the role '[role] nginx-reverse-proxy'
		%% End of the play 'play #4 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
