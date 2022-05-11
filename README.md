# fika-hugo-theme
Fika theme for Hugo

## Installation
### Step 1: Install Hugo with extended (Windows)
```bash
scoop install hugo-extended
```
### Step 2: Create site with `yaml` configuration
```bash
hugo new site quickstart -f yaml
```
### Step 3: Add Fika theme
```bash
cd quickstart
git init
git submodule add https://github.com/leaker/fika-hugo-theme.git themes/fika
```
Then, add Fika theme to the site configuration:
```bash
echo theme: \"fika\" >> config.yaml
```

## Configurations
In site configuration file: `config.yaml`
```yaml config.yaml
params:
  sub_title: # sub title for header
  logo: /image/logo.webp # header logo image. path to: /static/image/logo.webp
  cn_icp_id: # China Website Internet Content Provider ID. If site not deploy in china, keep empty

# header menu items
menu:
  main:
    - name: home
      title: HOME
      url: /
      identifier: home
      weight: 1
    - name: archives
      title: Archives
      url: /archives/index.html
      identifier: archives
      weight: 2
```

## How to use Archives Template
1. Create archives page
```bash
hugo new archives
```
2. Edit `/content/archives.md` and fill content
```markdown
---
title: Archives
layout: archives
hidden: true
url: /archives/index.html
---
```
**hidden: true** will make this page invisible with post list
