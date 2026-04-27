---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: false
weight: 100
name: "{{ .Name }}"
# `core`     — the main projects: editor, plugin marketplace, future
#              first-party SDKs.
# `support`  — adjacent tools that help you get into / out of Hugo
#              (migrations, scaffolders, converters).
category: "core"
repo: "https://github.com/hugo-tools/{{ .Name }}"
status: "active"
language: ""
description: ""
install: ""
homepage: ""
---

A longer description of what the project does. Shows up on the
project's detail page, not on the landing card.
