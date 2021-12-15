作者：forxhunter

[toc]
# 制作一个Project说明文档
成品大概长这个样子，[网站链接](https://forxhunter.github.io/PhysicsDIY/WebBuilt/GitPages/)
![result](GitPages.asset\result.png)
首先，默认你会一些基本的GitHub操作指南。如果不会，请注册一个[账号](github.com)，参考[QuickStart教程](https://docs.github.com/cn/get-started/quickstart)。
## 创建一个Repo
> 大部分翻译自：https://docs.github.com/cn/pages/quickstart
1. 在任何页面的右上角，使用  下拉菜单选择 New repository（新建仓库）。
    ![newrepo](GitPages.asset\create-repository-name-pages.png)

2. 输入`username.github.io`作为仓库的名字。

    记得替换`username`成你的名字。例如，如果你的名字是`octocat`，那么仓库名字就是`octocat.github.io`。
    > 当然，根据我的测试也可以起任何别的名字
    ![name](GitPages.asset\create-repository-name-pages.png)
3. 在仓库名称下，单击 Settings（设置）。
    ![sett](GitPages.asset\repo-actions-settings.png)
4. 左侧边栏中，往下滑选择Pages。
    ![pages](GitPages.asset\pages.png)
    首先，选择Source。一般选择`main/doc`。

    然后，需要选择一个主题。单机Theme跳转。如果不确定，就先随便选一个。
    ![theme](GitPages.asset\select-theme.png)
5. 选择主题后，您的存储库`README.md`文件将在文件编辑器中打开。该`README.md`文件是您为网站编写内容的地方。您可以暂时编辑文件或保留默认内容。
6. 完成文件编辑后，单击`Commit changes`。
7. 访问username.github.io以查看您的新网站。
    
注：对站点的更改在发送到 GitHub 后，可能需要 20 分钟才会发布。

如果网站地址不是username.github.io，那么可以回到设置Settings里面的Pages页面，最上面会显示该repo对应的网址。
![address](GitPages.asset\address_show.png)

## 更改标题和描述
鉴于这个不是重点，请参考[官方文档的描述](https://docs.github.com/cn/pages/quickstart#changing-the-title-and-description)

## 安装mkdocs并部署
通常，我们希望能创建一个侧边栏显示相关内容，但Gitpages的默认主题都只有顶边栏。如果觉得都可以，那么剩下的步骤都可以掠过了。

首先，放上MkDocs的[官方网站](https://www.mkdocs.org/getting-started/)

1. 安装mkdocs包
``` powershell
    pip install mkdocs
```
注：如果您发现任何错误，或者你都没有`pip`。请参考[官方说明](mkdocs.org/user-guide/installation/)

命令说明：
```powershell
    mkdocs --help
```
2. 将您的仓库克隆到本地便于操作。

3. 打开命令行，cd进入仓库中，创建`mkdocs.yml`文件使得你的Pages支持mkdocs。
相关文件逻辑如下：
``` markdown
./
    mkdocs.yml  # configuration file
    docs/
        index.md    # homepage
        ...         # other files needed
```
更改其中内容
