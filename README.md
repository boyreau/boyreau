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
	playbook_22b90657("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_96fccf77["play #1 (Get init process name): 4"]
		style play_96fccf77 stroke:#c1a60b,fill:#c1a60b,color:#ffffff
		playbook_22b90657 --> |"1"| play_96fccf77
		linkStyle 0 stroke:#c1a60b,color:#c1a60b
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Gitea personnal instance): 1'
		play_d59cba4b["play #2 (Gitea personnal instance): 1"]
		style play_d59cba4b stroke:#2412ba,fill:#2412ba,color:#ffffff
		playbook_22b90657 --> |"2"| play_d59cba4b
		linkStyle 1 stroke:#2412ba,color:#2412ba
			%% Start of the role '[role] gitea'
			play_d59cba4b --> |"1 "| role_49ff7bbe
			linkStyle 2 stroke:#2412ba,color:#2412ba
			role_49ff7bbe(["[role] gitea"])
			style role_49ff7bbe fill:#2412ba,color:#ffffff,stroke:#2412ba
			%% End of the role '[role] gitea'
		%% End of the play 'play #2 (Gitea personnal instance): 1'
		%% Start of the play 'play #3 (Gitea action runner): 1'
		play_5796dcff["play #3 (Gitea action runner): 1"]
		style play_5796dcff stroke:#287aa4,fill:#287aa4,color:#ffffff
		playbook_22b90657 --> |"3"| play_5796dcff
		linkStyle 3 stroke:#287aa4,color:#287aa4
			%% Start of the role '[role] go'
			play_5796dcff --> |"1 "| role_dd3ccb41
			linkStyle 4 stroke:#287aa4,color:#287aa4
			role_dd3ccb41(["[role] go"])
			style role_dd3ccb41 fill:#287aa4,color:#ffffff,stroke:#287aa4
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_5796dcff --> |"2 "| role_ba64518d
			linkStyle 5 stroke:#287aa4,color:#287aa4
			role_ba64518d(["[role] act_runner"])
			style role_ba64518d fill:#287aa4,color:#ffffff,stroke:#287aa4
			%% End of the role '[role] act_runner'
		%% End of the play 'play #3 (Gitea action runner): 1'
	%% End of the playbook './playbook.yaml'

```
