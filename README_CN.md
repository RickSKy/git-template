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
git cliff --latest --tag "Release 1.0.0"  # release to 1.0.0
git cliff --latest --tag "Beta 1.0.0"     # Beta 版本
```

### 格式说明
* demo 格式如下。demo描述： 新增功能 https filter (属于http模块), 关闭issue 12 和 issue 13
```bash
git commit -a -m "feat(http): #12 #13 https filter"

# 可选(http)
# 可选(#12 #13), issue 可以0个或者多个
```
* 支持的字段如下
  * feat: 新功能（feature）
  * fix: 修复bug
  * doc: 文档改变
  * style: 代码格式改变
  * refactor: 某个已有功能重构
  * perf: 性能优化
  * test: 增加测试, 主要指集成测试；单元测试应当在开发feat或者fix时创建
  * chore: 构建过程或辅助工具的变动



