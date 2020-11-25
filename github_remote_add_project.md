##                      Github通过Git命令远程给仓库上传文件

#### 一.Github上构建repositories(仓库)：

![new_a_repositiories](C:\Users\ASUS\Desktop\how_to_use_github\new_a_repositiories.png)

直接**New**一个你自己的存储库就可以了，下面就是需要填一些基本的仓库信息，包括名称，私人还是公共，是否需要添加一个README file等等，填完之后就创建了一个远程存储库，接下来你就可以把自己的项目部署在上面了。

![create_repositories](C:\Users\ASUS\Desktop\how_to_use_github\create_repositories.png)

**Important**：最好不要ADD a README file ，因为如果选择了最后你的项目就有两个分支了，建议刚开始就设置一个分支就好了

#### 二.Git：一个开源的分布式版本控制系统

简介：用于管理你的项目，它可以敏捷高效地处理任何大的或者是小的项目

**那么如何使用Git来将你的项目部署在远程地仓库中呢？**

完整的操作流程（亲测没有任何问题）挂个链接：https://blog.csdn.net/qq_39852676/article/details/99681382

首先找到你自己本地地项目文件，比如说我有一个在本地D盘的叫做Template的文件夹，我右键选择**git bash here**，就到了下面这个界面：

1.输入命令 `git init`，在你的文件夹下就会出现一个.git文件夹

2.输入命令 `git add .`  在我这儿出现了错误，我经过资料的查询发现是**符号转义**的问题，我可能讲述的不是特别详细，如果想更清楚的了解原因，可以移步至链接：https://blog.csdn.net/wq6ylg08/article/details/88761581

至于Windows平台下出现了这样的问题，其实不用过于担心，因为这个不影响最终在github上的项目上传

![git_1](C:\Users\ASUS\Desktop\how_to_use_github\git_1.png)

3.上一步就是把该文件夹下的所有的文件都git到仓库里面，接下来就是用`git commit -m "first commit"`，后面的说明可以自定义

![git_2](C:\Users\ASUS\Desktop\how_to_use_github\git_2.png)

4.需要一个SSH，我已经有了SSH，所以我就不需要再创建了，如果之前没有的话，通过如下的操作也可以自己创建一个SSH

![](C:\Users\ASUS\Desktop\how_to_use_github\git_3.png)

![git_4](C:\Users\ASUS\Desktop\how_to_use_github\git_4.png)

![git_5](C:\Users\ASUS\Desktop\how_to_use_github\git_5.png)

![git_4](C:\Users\ASUS\Desktop\how_to_use_github\git_4.png)![git_6](C:\Users\ASUS\Desktop\how_to_use_github\git_6.png)

5.创建好Git仓库之后我们就可以和本地的仓库进行关联了，通过 `git remote add origin`  后面是你的仓库地址，以**.git**结尾

![git_7](C:\Users\ASUS\Desktop\how_to_use_github\git_7.png)

6.关联好之后我们就可以把本地库的所有内容推送到远程仓库（也就是Github）上了，通过：git push  -u origin master （加入-u是因为新建的远程仓库是空的），等远程仓库里面有了内容之后，下次再从本地库上传内容的时候只需下面这样就可以了：

`git push origin master` 上传项目的过程可能需要等一段时间，完成之后是这样的：

![git_9](C:\Users\ASUS\Desktop\how_to_use_github\git_9.png)

好了，至此你就学会了如何通过git来上传你自己的项目了！！感谢各位观看！！！

