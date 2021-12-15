
@ #879273#基于django/neo4j的通讯录与QQ好友关系管理系统

> 本系统是分析手机同学录和QQ好友之间的可视化关系，基于neo4j这种图数据库，展示关系图谱，并基于echarts进行一些分析成果的展示以下是一些前期需求：
1.可以导入通讯录联系人，通讯录通话记录和QQ消息，读取本地文件，写入数据库和neo4j
2.通讯录联系人可视化（关系图谱）
3.通过权重分析，如聊天次数占1，通话次数占1，通话时长占2等权重设置，找到关键人物可视化出来  找出前三
4.用echart展示三幅图，一个是通讯录联系人分布（中国地图那张图），二是人物通话时长统计（柱状图），三是人物消息关键词频率统计（词云）
>
> 无论文
>
> 唯一
>
> 无安装录制视频

### 功能总览

脑图图片：![image.png](https://img-blog.csdnimg.cn/img_convert/e53c5a3a965c5019285832c296d492aa.png)

### 详细截图介绍

#### 登录注册退出
###### 登录
![image.png](https://img-blog.csdnimg.cn/img_convert/44d6d05c3f79cd6b28125280c11938a5.png)
###### 注册：
![image.png](https://img-blog.csdnimg.cn/img_convert/33793565111b866bc4cc10bdf0c18c79.png)
#### 联系人可视化
###### 我的联系人
![image.png](https://img-blog.csdnimg.cn/img_convert/f6f7291adb7a8166b0a8640c9a13041b.png)
###### 关键人物
![image.png](https://img-blog.csdnimg.cn/img_convert/f072c2f1601665ddbc557989d1af6d65.png)
#### 数据分析
###### 通讯录分布图
![image.png](https://img-blog.csdnimg.cn/img_convert/ccfb4cead9f9d9f23299259601ddc4cb.png)
###### 通话时长
![image.png](https://img-blog.csdnimg.cn/img_convert/19eca22951717efa95b1555b0feaccff.png)
###### QQ聊天词频
![image.png](https://img-blog.csdnimg.cn/img_convert/2a386dd93e0f35956924781c7b338219.png)



## 系统环境

| 环境    | 版本     | 下载链接 |
| ------- | -------- | -------- |
| windows | 所有版本 |          |
| python  | 3.7      | --       |
| neo4j   | --       | --       |

## 系统安装启动
系统采用django开发，全套使用django就可以，数据库为sqlite和neo4j
提前安装好neo4j
- 打开项目，安装python
- 安装依赖包: pip install -r need.txt -i https://mirrors.aliyun.com/pypi/simple/
- 启动django：python manage.py runserver
- 出现下图为成功：![image.png](https://img-blog.csdnimg.cn/img_convert/d0405bb475ac8d3633223708c3220938.png)


## 使用注意点
- 项目启动后，请先修改neo4j的账户密码，搜索全项目中所有 g=Graph('http://localhost:7474',user='neo4j',password='123456')
- 修改密码
- 初始化数据，访问下面四个链接
> http://localhost:8000/init_telephone

>http://localhost:8000/init_record

> http://localhost:8000/init_qq

> http://localhost:8000/init_neo4j


## 版权说明
本文谢绝转载，qalangtao.com
