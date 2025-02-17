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
	playbook_f6b427fa("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_7dc417cd["play #1 (Get init process name): 4"]
		style play_7dc417cd stroke:#537579,fill:#537579,color:#ffffff
		playbook_f6b427fa --> |"1"| play_7dc417cd
		linkStyle 0 stroke:#537579,color:#537579
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_94553fb6["play #2 (Mysql gitea database): 1"]
		style play_94553fb6 stroke:#5eba12,fill:#5eba12,color:#ffffff
		playbook_f6b427fa --> |"2"| play_94553fb6
		linkStyle 1 stroke:#5eba12,color:#5eba12
			%% Start of the role '[role] geerlingguy.mysql'
			play_94553fb6 --> |"1 "| role_f4800506
			linkStyle 2 stroke:#5eba12,color:#5eba12
			role_f4800506(["[role] geerlingguy.mysql"])
			style role_f4800506 fill:#5eba12,color:#ffffff,stroke:#5eba12
			%% End of the role '[role] geerlingguy.mysql'
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea instance): 1'
		play_41bc4592["play #3 (Gitea instance): 1"]
		style play_41bc4592 stroke:#ba125c,fill:#ba125c,color:#ffffff
		playbook_f6b427fa --> |"3"| play_41bc4592
		linkStyle 3 stroke:#ba125c,color:#ba125c
			%% Start of the role '[role] gitea'
			play_41bc4592 --> |"1 "| role_783e986b
			linkStyle 4 stroke:#ba125c,color:#ba125c
			role_783e986b(["[role] gitea"])
			style role_783e986b fill:#ba125c,color:#ffffff,stroke:#ba125c
			%% End of the role '[role] gitea'
		%% End of the play 'play #3 (Gitea instance): 1'
		%% Start of the play 'play #4 (Gitea action runner): 1'
		play_c3152f15["play #4 (Gitea action runner): 1"]
		style play_c3152f15 stroke:#c74005,fill:#c74005,color:#ffffff
		playbook_f6b427fa --> |"4"| play_c3152f15
		linkStyle 5 stroke:#c74005,color:#c74005
			%% Start of the role '[role] go'
			play_c3152f15 --> |"1 "| role_1b2fc5c3
			linkStyle 6 stroke:#c74005,color:#c74005
			role_1b2fc5c3(["[role] go"])
			style role_1b2fc5c3 fill:#c74005,color:#ffffff,stroke:#c74005
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_c3152f15 --> |"2 "| role_c27ca879
			linkStyle 7 stroke:#c74005,color:#c74005
			role_c27ca879(["[role] act_runner"])
			style role_c27ca879 fill:#c74005,color:#ffffff,stroke:#c74005
			%% End of the role '[role] act_runner'
		%% End of the play 'play #4 (Gitea action runner): 1'
		%% Start of the play 'play #5 (Nginx reverse proxy): 1'
		play_d02f0c32["play #5 (Nginx reverse proxy): 1"]
		style play_d02f0c32 stroke:#733b91,fill:#733b91,color:#ffffff
		playbook_f6b427fa --> |"5"| play_d02f0c32
		linkStyle 8 stroke:#733b91,color:#733b91
			%% Start of the role '[role] nginx_reverse_proxy'
			play_d02f0c32 --> |"1 "| role_3e82cb64
			linkStyle 9 stroke:#733b91,color:#733b91
			role_3e82cb64(["[role] nginx_reverse_proxy"])
			style role_3e82cb64 fill:#733b91,color:#ffffff,stroke:#733b91
			%% End of the role '[role] nginx_reverse_proxy'
		%% End of the play 'play #5 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
