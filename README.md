<h2 align="left">Hi 👋! My name is Arthur and I'm a DevOps, from France</h2>

###

<h3> My technical stack </h3>
<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ansible/ansible-original.svg" height="30" alt="Ansible logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" height="30" alt="Docker logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/githubactions/githubactions-original.svg" height="30" alt="GitHub Actions logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" height="30" alt="Bash logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="30" alt="Git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="30" alt="C logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/archlinux/archlinux-original.svg" height="30" alt="Arch Linux logo"  />
  <img width="12" />
</div>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=boyreau&hide_title=false&hide_rank=true&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=boyreau&locale=en&hide_title=false&count_private=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false&" height="150" alt="languages graph"  />
</div>

<h2> Meet me on </h2>

<div align="center">
  <a href="mailto:bnzlvosnb@mozmail.com">
    <img src="https://img.shields.io/static/v1?message=ProtonMail&logo=protonmail&label=&color=6D4AFF&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="proton mail logo"  />
  </a>
  <a href="https://www.linkedin.com/in/arthur-b-346985283">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo"  />
  </a>
  <a href="https://codeberg.org/zo">
    <img src="https://img.shields.io/static/v1?message=Codeberg&logo=codeberg&label=&color=4793CC&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="codeberg logo"  />
  </a>
</div>

<h2> I am currently deploying my own tools to improve my C codebase </h2>

<br clear="both">

```mermaid
architecture-beta
    group safe(database)[safe]
    group internal(server)[internal]
    group external(internet)[external]

        service mysql (database)[mysql] in safe

        service gitea (disk)[gitea] in internal
        service action_runner (server)[action_runner] in internal

        service nginx (internet)[nginx] in external

    gitea:R --> L:mysql
    nginx:R --> L:gitea
    action_runner:B --> T:gitea
```

###

<h3> This architecture will help me achieve the following workflow </h3>

```mermaid
---
title: My C devops pipeline
---
flowchart LR
    Develop["`**Develop**
Vim, Clangd, Git`"]
    Store_code["`**Version**
Gitea`"]
    Build["`**Build**
Github Actions, GNU Make, LLVM Clang`"]
    Test["`**Test**
LLVM Toolchain, GNU Make`"]
    Store_artifacts["`**Store**
Conan (WIP)`"]
    Deploy["`**Deploy**
Ansible, Docker`"]
    Monitor["`**Monitor**
Grafana (WIP)`"]

    Develop --> Store_code --> Build --> Test --> Store_artifacts --> Deploy --> Monitor
```

<h3> And here is a graph of my ansible configuration </h3>

```mermaid
---
title: "My super-well-designed Ansible mess"
---
%%{ init: { "flowchart": { "curve": "bumpX" } } }%%
flowchart LR
	%% Start of the playbook './playbook.yaml'
	playbook_8e31b498("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_5dee4b89["play #1 (Get init process name): 4"]
		style play_5dee4b89 stroke:#02ca9b,fill:#02ca9b,color:#ffffff
		playbook_8e31b498 --> |"1"| play_5dee4b89
		linkStyle 0 stroke:#02ca9b,color:#02ca9b
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_dff30eec["play #2 (Mysql gitea database): 1"]
		style play_dff30eec stroke:#41528b,fill:#41528b,color:#ffffff
		playbook_8e31b498 --> |"2"| play_dff30eec
		linkStyle 1 stroke:#41528b,color:#41528b
			%% Start of the role '[role] geerlingguy.mysql'
			play_dff30eec --> |"1 "| role_cb4d0091
			linkStyle 2 stroke:#41528b,color:#41528b
			role_cb4d0091(["[role] geerlingguy.mysql"])
			style role_cb4d0091 fill:#41528b,color:#ffffff,stroke:#41528b
			%% End of the role '[role] geerlingguy.mysql'
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea instance): 1'
		play_515c3c4a["play #3 (Gitea instance): 1"]
		style play_515c3c4a stroke:#b54c17,fill:#b54c17,color:#ffffff
		playbook_8e31b498 --> |"3"| play_515c3c4a
		linkStyle 3 stroke:#b54c17,color:#b54c17
			%% Start of the role '[role] gitea'
			play_515c3c4a --> |"1 "| role_5e5f790c
			linkStyle 4 stroke:#b54c17,color:#b54c17
			role_5e5f790c(["[role] gitea"])
			style role_5e5f790c fill:#b54c17,color:#ffffff,stroke:#b54c17
			%% End of the role '[role] gitea'
		%% End of the play 'play #3 (Gitea instance): 1'
		%% Start of the play 'play #4 (Gitea action runner): 1'
		play_09b411b8["play #4 (Gitea action runner): 1"]
		style play_09b411b8 stroke:#13b9a6,fill:#13b9a6,color:#ffffff
		playbook_8e31b498 --> |"4"| play_09b411b8
		linkStyle 5 stroke:#13b9a6,color:#13b9a6
			%% Start of the role '[role] go'
			play_09b411b8 --> |"1 "| role_13ad03b6
			linkStyle 6 stroke:#13b9a6,color:#13b9a6
			role_13ad03b6(["[role] go"])
			style role_13ad03b6 fill:#13b9a6,color:#ffffff,stroke:#13b9a6
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_09b411b8 --> |"2 "| role_77461e1a
			linkStyle 7 stroke:#13b9a6,color:#13b9a6
			role_77461e1a(["[role] act_runner"])
			style role_77461e1a fill:#13b9a6,color:#ffffff,stroke:#13b9a6
			%% End of the role '[role] act_runner'
		%% End of the play 'play #4 (Gitea action runner): 1'
		%% Start of the play 'play #5 (Nginx reverse proxy): 1'
		play_ed76da53["play #5 (Nginx reverse proxy): 1"]
		style play_ed76da53 stroke:#0cc0bd,fill:#0cc0bd,color:#ffffff
		playbook_8e31b498 --> |"5"| play_ed76da53
		linkStyle 8 stroke:#0cc0bd,color:#0cc0bd
			%% Start of the role '[role] nginx_reverse_proxy'
			play_ed76da53 --> |"1 "| role_ee517261
			linkStyle 9 stroke:#0cc0bd,color:#0cc0bd
			role_ee517261(["[role] nginx_reverse_proxy"])
			style role_ee517261 fill:#0cc0bd,color:#ffffff,stroke:#0cc0bd
			%% End of the role '[role] nginx_reverse_proxy'
		%% End of the play 'play #5 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
