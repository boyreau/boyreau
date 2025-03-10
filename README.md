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
  <img src="https://github-readme-stats.vercel.app/api?username=boyreau&hide_title=false&hide_rank=true&show_icons=true&include_all_commits=false&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false&" height="150" alt="stats graph"  />
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
	playbook_33ba7ad3("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_2640d476["play #1 (Get init process name): 4"]
		style play_2640d476 stroke:#115cbb,fill:#115cbb,color:#ffffff
		playbook_33ba7ad3 --> |"1"| play_2640d476
		linkStyle 0 stroke:#115cbb,color:#115cbb
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_106aa22b["play #2 (Mysql gitea database): 1"]
		style play_106aa22b stroke:#c10b96,fill:#c10b96,color:#ffffff
		playbook_33ba7ad3 --> |"2"| play_106aa22b
		linkStyle 1 stroke:#c10b96,color:#c10b96
			%% Start of the role '[role] geerlingguy.mysql'
			play_106aa22b --> |"1 "| role_646d49a6
			linkStyle 2 stroke:#c10b96,color:#c10b96
			role_646d49a6(["[role] geerlingguy.mysql"])
			style role_646d49a6 fill:#c10b96,color:#ffffff,stroke:#c10b96
			%% End of the role '[role] geerlingguy.mysql'
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea instance): 1'
		play_2209cbb5["play #3 (Gitea instance): 1"]
		style play_2209cbb5 stroke:#8d6e3f,fill:#8d6e3f,color:#ffffff
		playbook_33ba7ad3 --> |"3"| play_2209cbb5
		linkStyle 3 stroke:#8d6e3f,color:#8d6e3f
			%% Start of the role '[role] gitea'
			play_2209cbb5 --> |"1 "| role_87dd78d0
			linkStyle 4 stroke:#8d6e3f,color:#8d6e3f
			role_87dd78d0(["[role] gitea"])
			style role_87dd78d0 fill:#8d6e3f,color:#ffffff,stroke:#8d6e3f
			%% End of the role '[role] gitea'
		%% End of the play 'play #3 (Gitea instance): 1'
		%% Start of the play 'play #4 (Gitea action runner): 1'
		play_e545f438["play #4 (Gitea action runner): 1"]
		style play_e545f438 stroke:#b24b1a,fill:#b24b1a,color:#ffffff
		playbook_33ba7ad3 --> |"4"| play_e545f438
		linkStyle 5 stroke:#b24b1a,color:#b24b1a
			%% Start of the role '[role] go'
			play_e545f438 --> |"1 "| role_ed960b33
			linkStyle 6 stroke:#b24b1a,color:#b24b1a
			role_ed960b33(["[role] go"])
			style role_ed960b33 fill:#b24b1a,color:#ffffff,stroke:#b24b1a
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_e545f438 --> |"2 "| role_535082b9
			linkStyle 7 stroke:#b24b1a,color:#b24b1a
			role_535082b9(["[role] act_runner"])
			style role_535082b9 fill:#b24b1a,color:#ffffff,stroke:#b24b1a
			%% End of the role '[role] act_runner'
		%% End of the play 'play #4 (Gitea action runner): 1'
		%% Start of the play 'play #5 (Nginx reverse proxy): 1'
		play_ea0e6d47["play #5 (Nginx reverse proxy): 1"]
		style play_ea0e6d47 stroke:#ba2712,fill:#ba2712,color:#ffffff
		playbook_33ba7ad3 --> |"5"| play_ea0e6d47
		linkStyle 8 stroke:#ba2712,color:#ba2712
			%% Start of the role '[role] nginx_reverse_proxy'
			play_ea0e6d47 --> |"1 "| role_48e37873
			linkStyle 9 stroke:#ba2712,color:#ba2712
			role_48e37873(["[role] nginx_reverse_proxy"])
			style role_48e37873 fill:#ba2712,color:#ffffff,stroke:#ba2712
			%% End of the role '[role] nginx_reverse_proxy'
		%% End of the play 'play #5 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
