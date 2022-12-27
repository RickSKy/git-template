### 基本说明
* 本git-template 配置主要用于适配 [git-cliff](https://github.com/orhun/git-cliff) 的默认配置。 同时适配于 gitlab 的自动关闭issue

### 使用步骤
* PC首次配置，需要全局配置本地git
```bash
git clone https://github.com/RickSKy/git-template ~/.git-template
git config --global init.templatedir '~/.git-template'
```
* 每个仓库目录下，需要运行以下命令，用于同步本地配置至当前仓库的.git
```
git init
```
* 后续每次生成changelog 运行以下命令即可
```bash 
git cliff --latest    # not release, 
git cliff --latest --tag 1.0.0 # release to 1.0.0
```


