# git 指令

- git init: 初始化目录
- -rm -rf .git: 删除.git 文件夹等于删除仓库
- git clone [address]: 克隆仓库
- git diff --cached <file>: 暂存区和最后一次提交(HEAD)差异
- git commit -m "信息": 提交 -m 指定提交注释
- git log: 提交记录
- git reset: 回退版本

## 特殊

- cached: 通常和暂存区有关

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

2. git reset 回退

- git reset --soft: 同时保留工作区和暂存区内容
- git reset --hard: 不保留工作区和暂存区内容
- git reset --mixed: 保留工作区, 不保留暂存区
- git reset HEAD^: 等于 mixed

3. git diff 不同

- git diff <file>: 比较工作区和暂存区差异
- git diff HEAD <file>: 比较工作区和版本库差异
- git diff --cached <file>: 比较暂存区和版本库差异
- git diff HEAD~[数字-前几个版本] HEAD: 上两个版本

4. 删除文件

- rm <file>: 本地删除文件
- git rm <file>: 暂存区删除
- git rm --cached <file>: 暂存区删除, 工作区不同

# .gitignore

- 系统或者软件自动生成的文件
- 编译产生的中间文件和结果文件
- 忽略日志文件和文件夹
- 忽略 .class 文件夹 / .o / .env / .zip / tar / .pem 文件
- 运行的日志文件, 缓存文件, 临时文件
