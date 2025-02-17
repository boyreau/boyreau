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

