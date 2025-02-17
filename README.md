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
	playbook_1850d60d("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_564159c9["play #1 (Get init process name): 4"]
		style play_564159c9 stroke:#c8c604,fill:#c8c604,color:#ffffff
		playbook_1850d60d --> |"1"| play_564159c9
		linkStyle 0 stroke:#c8c604,color:#c8c604
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_3fe2b7e2["play #2 (Mysql gitea database): 1"]
		style play_3fe2b7e2 stroke:#1a1eb2,fill:#1a1eb2,color:#ffffff
		playbook_1850d60d --> |"2"| play_3fe2b7e2
		linkStyle 1 stroke:#1a1eb2,color:#1a1eb2
			%% Start of the role '[role] geerlingguy.mysql'
			play_3fe2b7e2 --> |"1 "| role_79d39041
			linkStyle 2 stroke:#1a1eb2,color:#1a1eb2
			role_79d39041(["[role] geerlingguy.mysql"])
			style role_79d39041 fill:#1a1eb2,color:#ffffff,stroke:#1a1eb2
			%% End of the role '[role] geerlingguy.mysql'
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_915a83be["play #3 (Gitea action runner): 1"]
		style play_915a83be stroke:#c2c705,fill:#c2c705,color:#ffffff
		playbook_1850d60d --> |"3"| play_915a83be
		linkStyle 3 stroke:#c2c705,color:#c2c705
			%% Start of the role '[role] go'
			play_915a83be --> |"1 "| role_bc85eb9c
			linkStyle 4 stroke:#c2c705,color:#c2c705
			role_bc85eb9c(["[role] go"])
			style role_bc85eb9c fill:#c2c705,color:#ffffff,stroke:#c2c705
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_915a83be --> |"2 "| role_d35d1a18
			linkStyle 5 stroke:#c2c705,color:#c2c705
			role_d35d1a18(["[role] act_runner"])
			style role_d35d1a18 fill:#c2c705,color:#ffffff,stroke:#c2c705
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
		%% Start of the play 'play #4 (Nginx reverse proxy): 1'
		play_6bf47ea1["play #4 (Nginx reverse proxy): 1"]
		style play_6bf47ea1 stroke:#bf0da6,fill:#bf0da6,color:#ffffff
		playbook_1850d60d --> |"4"| play_6bf47ea1
		linkStyle 6 stroke:#bf0da6,color:#bf0da6
			%% Start of the role '[role] nginx-reverse-proxy'
			play_6bf47ea1 --> |"1 "| role_cc9dbc68
			linkStyle 7 stroke:#bf0da6,color:#bf0da6
			role_cc9dbc68(["[role] nginx-reverse-proxy"])
			style role_cc9dbc68 fill:#bf0da6,color:#ffffff,stroke:#bf0da6
			%% End of the role '[role] nginx-reverse-proxy'
		%% End of the play 'play #4 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
