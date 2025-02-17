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
	playbook_5ab0c368("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_7a2b1a52["play #1 (Get init process name): 4"]
		style play_7a2b1a52 stroke:#1fabad,fill:#1fabad,color:#ffffff
		playbook_5ab0c368 --> |"1"| play_7a2b1a52
		linkStyle 0 stroke:#1fabad,color:#1fabad
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_05e8e6df["play #2 (Mysql gitea database): 1"]
		style play_05e8e6df stroke:#11a1bb,fill:#11a1bb,color:#ffffff
		playbook_5ab0c368 --> |"2"| play_05e8e6df
		linkStyle 1 stroke:#11a1bb,color:#11a1bb
			%% Start of the role '[role] geerlingguy.mysql'
			play_05e8e6df --> |"1 "| role_b706d36c
			linkStyle 2 stroke:#11a1bb,color:#11a1bb
			role_b706d36c(["[role] geerlingguy.mysql"])
			style role_b706d36c fill:#11a1bb,color:#ffffff,stroke:#11a1bb
			%% End of the role '[role] geerlingguy.mysql'
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea instance): 1'
		play_9807b153["play #3 (Gitea instance): 1"]
		style play_9807b153 stroke:#3018b4,fill:#3018b4,color:#ffffff
		playbook_5ab0c368 --> |"3"| play_9807b153
		linkStyle 3 stroke:#3018b4,color:#3018b4
			%% Start of the role '[role] gitea'
			play_9807b153 --> |"1 "| role_d1c16844
			linkStyle 4 stroke:#3018b4,color:#3018b4
			role_d1c16844(["[role] gitea"])
			style role_d1c16844 fill:#3018b4,color:#ffffff,stroke:#3018b4
			%% End of the role '[role] gitea'
		%% End of the play 'play #3 (Gitea instance): 1'
		%% Start of the play 'play #4 (Gitea action runner): 1'
		play_3b628fc7["play #4 (Gitea action runner): 1"]
		style play_3b628fc7 stroke:#7a4587,fill:#7a4587,color:#ffffff
		playbook_5ab0c368 --> |"4"| play_3b628fc7
		linkStyle 5 stroke:#7a4587,color:#7a4587
			%% Start of the role '[role] go'
			play_3b628fc7 --> |"1 "| role_5090f880
			linkStyle 6 stroke:#7a4587,color:#7a4587
			role_5090f880(["[role] go"])
			style role_5090f880 fill:#7a4587,color:#ffffff,stroke:#7a4587
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_3b628fc7 --> |"2 "| role_d278f23b
			linkStyle 7 stroke:#7a4587,color:#7a4587
			role_d278f23b(["[role] act_runner"])
			style role_d278f23b fill:#7a4587,color:#ffffff,stroke:#7a4587
			%% End of the role '[role] act_runner'
		%% End of the play 'play #4 (Gitea action runner): 1'
		%% Start of the play 'play #5 (Nginx reverse proxy): 1'
		play_9ea87add["play #5 (Nginx reverse proxy): 1"]
		style play_9ea87add stroke:#7eac20,fill:#7eac20,color:#ffffff
		playbook_5ab0c368 --> |"5"| play_9ea87add
		linkStyle 8 stroke:#7eac20,color:#7eac20
			%% Start of the role '[role] nginx-reverse-proxy'
			play_9ea87add --> |"1 "| role_627a7854
			linkStyle 9 stroke:#7eac20,color:#7eac20
			role_627a7854(["[role] nginx-reverse-proxy"])
			style role_627a7854 fill:#7eac20,color:#ffffff,stroke:#7eac20
			%% End of the role '[role] nginx-reverse-proxy'
		%% End of the play 'play #5 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
