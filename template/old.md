## Hi 👋! My name is Arthur and I'm a student

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

