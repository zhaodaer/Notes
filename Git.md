#### 使用Git工具将本地代码推送到GitHub远程仓库的具体步骤如下：

1. 在本地项目文件夹打开Git Bash
2. git init             初始化git仓库
3. git add .          将项目文件夹所有文件放入暂存区
4. git commit -m “第二次修改”         提交项目文件夹所有文件-提交文件
5. git remote add origin git@github.com:zhaodaer/Notes.git   添加远程连接
6. git pull origin main           // 把本地仓库的变化连接到远程仓库main
7. git push -u origin main       //把本地仓库的文件推送到远程仓库main



若出现error: remote origin already exists.

则 ``git remote rm origin `` 删除关联的origin的远程库



**复制一下代码，推送到远程仓库：**

```c
git remote rm origin
git init
git add . 
git commit -m “第N次修改” 
git remote add origin git@github.com:zhaodaer/Notes.git
git pull origin main
git push -u origin main
```



