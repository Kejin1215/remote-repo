# git 指令

- git init: 初始化目录
- -rm -rf .git: 删除.git 文件夹等于删除仓库
- git clone [address]: 克隆仓库
- git diff --cached <file>: 暂存区和最后一次提交(HEAD)差异

# 三大区

- 工作区: 电脑上的目录, 正操作的文件夹
- 暂存区: 临时存储区域, 保存即将提交到 git 仓库的修改内容
- 本地仓库: git init 创建的目录, 包含了完整的项目历史和元数据, git 存储代码和版本
  信息的主要位置
- 工作区 git add -> 暂存区 git commit -> 本地仓库

# git 文件状态

- 未跟踪: 新创建未管理
- 未修改: 跟踪未修改
- 已修改: 修改未添加暂存区
- 已暂存: 修改并添加暂存区

# 操作尝试

1. 撤销暂存

- 编辑的文件在工作区, add 之后在暂存区, 取消暂存用 git rm --cached <file>
- 但是 add 之后再更改的话取消暂存会失败, 需要统一版本
- 最新版本: 重新 git add
- 版本回滚: git checkout -- <file>
