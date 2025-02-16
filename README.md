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
	playbook_90361684("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_d88f6aa0["play #1 (Get init process name): 4"]
		style play_d88f6aa0 stroke:#16a7b6,fill:#16a7b6,color:#ffffff
		playbook_90361684 --> |"1"| play_d88f6aa0
		linkStyle 0 stroke:#16a7b6,color:#16a7b6
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_80ffd5fb["play #2 (Mysql gitea database): 1"]
		style play_80ffd5fb stroke:#348998,fill:#348998,color:#ffffff
		playbook_90361684 --> |"2"| play_80ffd5fb
		linkStyle 1 stroke:#348998,color:#348998
			%% Start of the role '[role] geerlingguy.mysql'
			play_80ffd5fb --> |"1 "| role_0b6b4a30
			linkStyle 2 stroke:#348998,color:#348998
			role_0b6b4a30(["[role] geerlingguy.mysql"])
			style role_0b6b4a30 fill:#348998,color:#ffffff,stroke:#348998
			%% End of the role '[role] geerlingguy.mysql'
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_46cd6bd6["play #3 (Gitea action runner): 1"]
		style play_46cd6bd6 stroke:#03c940,fill:#03c940,color:#ffffff
		playbook_90361684 --> |"3"| play_46cd6bd6
		linkStyle 3 stroke:#03c940,color:#03c940
			%% Start of the role '[role] go'
			play_46cd6bd6 --> |"1 "| role_0ff4c388
			linkStyle 4 stroke:#03c940,color:#03c940
			role_0ff4c388(["[role] go"])
			style role_0ff4c388 fill:#03c940,color:#ffffff,stroke:#03c940
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_46cd6bd6 --> |"2 "| role_d20c53b4
			linkStyle 5 stroke:#03c940,color:#03c940
			role_d20c53b4(["[role] act_runner"])
			style role_d20c53b4 fill:#03c940,color:#ffffff,stroke:#03c940
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
		%% Start of the play 'play #4 (Nginx reverse proxy): 1'
		play_c226a73e["play #4 (Nginx reverse proxy): 1"]
		style play_c226a73e stroke:#57755f,fill:#57755f,color:#ffffff
		playbook_90361684 --> |"4"| play_c226a73e
		linkStyle 6 stroke:#57755f,color:#57755f
			%% Start of the role '[role] nginx-reverse-proxy'
			play_c226a73e --> |"1 "| role_765411cd
			linkStyle 7 stroke:#57755f,color:#57755f
			role_765411cd(["[role] nginx-reverse-proxy"])
			style role_765411cd fill:#57755f,color:#ffffff,stroke:#57755f
			%% End of the role '[role] nginx-reverse-proxy'
		%% End of the play 'play #4 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
