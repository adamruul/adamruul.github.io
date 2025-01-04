# :globe_with_meridians: [**`adamruul.github.io`**](https://adamruul.github.io/)

Personal website used for various things. The website is built using [Hugo](https://gohugo.io/) (with the [Blowfish theme](https://github.com/nunocoracao/blowfish))

## Prerequisites
In order to build the website locally you need to have [Hugo](https://gohugo.io/installation) installed.


## Deployment

The deployment is handled via a GitHub Action. The deployment action is automatically triggered on changes to the `master` branch.


## Write a new post

1. Clone the repository.
2. Add or edit the markdown files under `content/`
3. `git add --all && git commit -m "your message"`
4. `git push origin master`

## Update layout or other settings

1. Clone the repository.
2. Change the parameters in `config/_default/`
3. Build the site by simply running: `hugo`
4. `git add --all && git commit -m "your message"`
5. `git push origin master`


## Obsidian integration
Posts can be published directly from [Obsidian](https://obsidian.md/) using the [Enveloppe plugin](https://github.com/Enveloppe/obsidian-enveloppe). To publish a Note from Obsidian, add the following front-matter:
```
---
share: true
title: "My First Obsidian Blog Post"
date: "2025-01-04"
draft: false
---
```
> The property `share: true` will signal to Enveloppe that this note should be published.

Then run the Obsidian command `Enveloppe: Upload all shared notes`

> _this^ command will push **all** shared Notes._

Note will be converted into a Hugo compatible markdown file... and placed under `content/blog/`. The plugin will create a Pull Request and automatically merge it.
