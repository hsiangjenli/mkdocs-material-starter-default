# Mkdocs
## Setup

```python
mkdocs new .
```

> **會新增兩個file/folder**  
> 1. mkdocs.yml --> setup your website, extension.  
> 2. docs --> The place you can storage your markdown files.  

![](https://i.imgur.com/7GnQMm1.png)

### Logo/Favicon設定

```yaml
├─docs
│  └─assets
│      └─images
│          └─my-dragon-solid.svg
├─mkdocs.yml
```

```yaml
theme:
...
  logo: assets/images/my-dragon-solid.svg
  favicon: assets/images/my-dragon-solid.svg
```
### 顏色設定
1. 基本
```yaml
theme:
...
  palette:
    primary: blue grey # 主色系
    accent: indigo # 超連結顏色
```

2. 亮色/暗色模式
```yaml
theme:
...
  palette:
    - scheme: default
      primary: blue grey
      accent: indigo
      toggle:
        icon: material/toggle-switch-off-outline 
        name: Switch to dark mode
    
    - scheme: slate 
      primary: black
      accent: indigo
      toggle:
        icon: material/toggle-switch
        name: Switch to light mode
```
### Header 設定
1. 新增repo
```yaml
repo_url: # repository url
repo_name: # display name
...
theme:
```
### [Footer 設定](https://squidfunk.github.io/mkdocs-material/setup/setting-up-the-footer/)
1. Social icons
```yaml
theme:
...
extra:
  social:
    - icon: fontawesome/brands/github 
      link: https://github.com/{#id}
    - icon: fontawesome/solid/paper-plane
      link: mailto:{#email}
    - icon: fontawesome/solid/globe
      link: https://{#id}.github.io/
    - icon: fontawesome/brands/linkedin
      link: https://www.linkedin.com/in/{#id}/
```
### Additional CSS
```yaml
├─docs
│  ├─assets
│  │  └─images
│  ├─stylesheets
│  │      └─mycss.css
```
```yaml
theme:
...
extra_css:
  - stylesheets/mycss.css # import your custom css files.
```