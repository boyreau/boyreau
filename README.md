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
	playbook_46c6d4d9("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_1eb6c2ff["play #1 (Get init process name): 4"]
		style play_1eb6c2ff stroke:#2ba131,fill:#2ba131,color:#ffffff
		playbook_46c6d4d9 --> |"1"| play_1eb6c2ff
		linkStyle 0 stroke:#2ba131,color:#2ba131
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_5021d4b1["play #2 (Gitea personnal instance): 1"]
		style play_5021d4b1 stroke:#43923a,fill:#43923a,color:#ffffff
		playbook_46c6d4d9 --> |"2"| play_5021d4b1
		linkStyle 1 stroke:#43923a,color:#43923a
			%% Start of the role '[role] gitea'
			play_5021d4b1 --> |"1 "| role_f388aca4
			linkStyle 2 stroke:#43923a,color:#43923a
			role_f388aca4(["[role] gitea"])
			style role_f388aca4 fill:#43923a,color:#ffffff,stroke:#43923a
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_da759632["play #3 (Gitea action runner): 1"]
		style play_da759632 stroke:#22aa28,fill:#22aa28,color:#ffffff
		playbook_46c6d4d9 --> |"3"| play_da759632
		linkStyle 3 stroke:#22aa28,color:#22aa28
			%% Start of the role '[role] go'
			play_da759632 --> |"1 "| role_91a6f8be
			linkStyle 4 stroke:#22aa28,color:#22aa28
			role_91a6f8be(["[role] go"])
			style role_91a6f8be fill:#22aa28,color:#ffffff,stroke:#22aa28
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_da759632 --> |"2 "| role_99b9d617
			linkStyle 5 stroke:#22aa28,color:#22aa28
			role_99b9d617(["[role] act_runner"])
			style role_99b9d617 fill:#22aa28,color:#ffffff,stroke:#22aa28
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
	%% End of the playbook './playbook.yaml'

```
