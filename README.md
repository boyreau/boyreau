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
	playbook_1f1583a3("./playbook.yaml")
		%% Start of the play 'play #1 (Get init process name): 4'
		play_66935978["play #1 (Get init process name): 4"]
		style play_66935978 stroke:#450fbd,fill:#450fbd,color:#ffffff
		playbook_1f1583a3 --> |"1"| play_66935978
		linkStyle 0 stroke:#450fbd,color:#450fbd
		%% End of the play 'play #1 (Get init process name): 4'
		%% Start of the play 'play #2 (Mysql gitea database): 1'
		play_a13ce724["play #2 (Mysql gitea database): 1"]
		style play_a13ce724 stroke:#4b7181,fill:#4b7181,color:#ffffff
		playbook_1f1583a3 --> |"2"| play_a13ce724
		linkStyle 1 stroke:#4b7181,color:#4b7181
			%% Start of the role '[role] geerlingguy.mysql'
			play_a13ce724 --> |"1 "| role_321ea4e3
			linkStyle 2 stroke:#4b7181,color:#4b7181
			role_321ea4e3(["[role] geerlingguy.mysql"])
			style role_321ea4e3 fill:#4b7181,color:#ffffff,stroke:#4b7181
			%% End of the role '[role] geerlingguy.mysql'
		%% End of the play 'play #2 (Mysql gitea database): 1'
		%% Start of the play 'play #3 (Gitea instance): 1'
		play_c54bb46f["play #3 (Gitea instance): 1"]
		style play_c54bb46f stroke:#527a6c,fill:#527a6c,color:#ffffff
		playbook_1f1583a3 --> |"3"| play_c54bb46f
		linkStyle 3 stroke:#527a6c,color:#527a6c
			%% Start of the role '[role] gitea'
			play_c54bb46f --> |"1 "| role_d57423ee
			linkStyle 4 stroke:#527a6c,color:#527a6c
			role_d57423ee(["[role] gitea"])
			style role_d57423ee fill:#527a6c,color:#ffffff,stroke:#527a6c
			%% End of the role '[role] gitea'
		%% End of the play 'play #3 (Gitea instance): 1'
		%% Start of the play 'play #4 (Gitea action runner): 1'
		play_68d90d59["play #4 (Gitea action runner): 1"]
		style play_68d90d59 stroke:#1371b9,fill:#1371b9,color:#ffffff
		playbook_1f1583a3 --> |"4"| play_68d90d59
		linkStyle 5 stroke:#1371b9,color:#1371b9
			%% Start of the role '[role] go'
			play_68d90d59 --> |"1 "| role_ed0afad2
			linkStyle 6 stroke:#1371b9,color:#1371b9
			role_ed0afad2(["[role] go"])
			style role_ed0afad2 fill:#1371b9,color:#ffffff,stroke:#1371b9
			%% End of the role '[role] go'
			%% Start of the role '[role] act_runner'
			play_68d90d59 --> |"2 "| role_3d26f975
			linkStyle 7 stroke:#1371b9,color:#1371b9
			role_3d26f975(["[role] act_runner"])
			style role_3d26f975 fill:#1371b9,color:#ffffff,stroke:#1371b9
			%% End of the role '[role] act_runner'
		%% End of the play 'play #4 (Gitea action runner): 1'
		%% Start of the play 'play #5 (Nginx reverse proxy): 1'
		play_ed8e7ff6["play #5 (Nginx reverse proxy): 1"]
		style play_ed8e7ff6 stroke:#1eae55,fill:#1eae55,color:#ffffff
		playbook_1f1583a3 --> |"5"| play_ed8e7ff6
		linkStyle 8 stroke:#1eae55,color:#1eae55
			%% Start of the role '[role] nginx_reverse_proxy'
			play_ed8e7ff6 --> |"1 "| role_0e60a90c
			linkStyle 9 stroke:#1eae55,color:#1eae55
			role_0e60a90c(["[role] nginx_reverse_proxy"])
			style role_0e60a90c fill:#1eae55,color:#ffffff,stroke:#1eae55
			%% End of the role '[role] nginx_reverse_proxy'
		%% End of the play 'play #5 (Nginx reverse proxy): 1'
	%% End of the playbook './playbook.yaml'

```
