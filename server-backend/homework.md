### 2018后端培训作业

---

#### 作业一（必做）

* 利用python下的requests包体验两种http请求的方式，如果没有安装这个包的话，用pip install安装即可
* 可以尝试的链接如下：（强调：一定要加最后的slash“/”）
    * get:
        * https://ts19.eesast.com
        * https://ts19.eesast.com/backend/teams/allteam/
        * https://ts19.eesast.com/backend/download/allfiles/
    * post:
        * https://ts19.eesast.com/backend/teams/oneteam/
        * https://ts19.eesast.com/backend/teams/score/
        * https://ts19.eesast.com/backend/students/leader/
* 参考代码如下：（可以直接在python终端运行，不用写成脚本，视自身情况而定）
```
    import requests

    r = requests.get(https://ts19.eesast.com/backend/download/allfiles/)
    print(r.text) #终端里可以直接用r.text查看其内容
```
* 作业以文档形式提交，文档中列出至少一个你用requests尝试get或post的链接及链接内容，建议大家上网查找requests这个实体的所有属性及其内容，若能在报告中列出其他属性就更好啦
* 请大家将作业邮件发到13935047516@163.com，以【姓名_后端作业】作为邮件名
* 截止日期2018.7.20

#### 作业二（有志于开发网站的同学必做）

* 完成django 官网 tutorials的内容https://docs.djangoproject.com/en/2.0/intro/tutorial01/
* 参照官方文档，阅读github上team18Web仓库的代码，也可以参照team19的代码，完成以下任务：
    * 掌握单项目多app的架构，了解多个app是如何统一到一个项目下的
    * 了解该项目下每个app的功能是什么
    * 阅读login的内容，了解login应当完成哪些操作
* 和负责前端的同学共同完成一个注册登录功能