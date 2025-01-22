# Storming

### ————基于大语言模型的热门IP化讲解系统

## 关于本项目

![image-20250122101631054](C:\Users\chenxiuxiu\AppData\Roaming\Typora\typora-user-images\image-20250122101631054.png)

### 构建工具

本项目使用的主要框架或库。

前端：

- [React.js](https://reactjs.org/)
- [Vue.js](https://vuejs.org/)

后端：

- [Flask](https://flask.palletsprojects.com/en/latest/)
- [LangChain](https://www.langchain.com/)

数据库：

- [Weaviate](https://weaviate.io/)
- [MySQL](https://www.mysql.com/)

## 开始

这是一份在本地构建项目的指导的例子。 要获取本地副本并且配置运行，你可以按照下面的示例步骤操作。

### 项目结构

```python
app/                   
+-- backend -----------------------# 后端              
|   +-- .env                   
|   +-- config.py                  
|   +-- db.py                      # 数据库接口
|   +-- Dockerfile                
|   +-- generator.py               # 数据生成接口
|   +-- graph.py                   # 图相关操作文件     
|   +-- main.py                    
|   +-- models.py                 
|   +-- requirements.txt     
|   +-- test_weaviate.py           # Weaviate 测试脚本
|   +-- utils.py               
+-- static                         # 静态资源目录
|   +-- css                    
|   |   +-- main.3c357a7b.css     
|	|   +-- ···
+--templates-----------------------# 前端               
|   +-- index.html                 # 主 HTML 文件
|   +-- ···
+-- docker-compose.yml             # Docker Compose 配置文件
+--.env      
```

### 依赖

`NPM`

```json
"@ant-design/charts": "^2.2.6",
"antd": "5.0",
"axios": "^1.7.9",
"cra-template": "1.2.0",
"dayjs": "^1.11.13",
"fetch-jsonp": "^1.3.0",
"lodash": "^4.17.21",
"qs": "^6.13.1",
"react": "^19.0.0",
"react-dom": "^19.0.0",
"react-markdown": "^9.0.3",
"react-router": "^7.1.3",
"react-router-dom": "^7.1.3",
"react-scripts": "5.0.1",
"sass": "^1.83.1",
"web-vitals": "^4.2.4"
```

`Python`

```python
Flask==3.1.0
flask_cors==5.0.0
langchain==0.3.15
langchain_community==0.3.15
langchain_core==0.3.31
langchain_openai==0.3.1
langchain_text_splitters==0.3.5
langgraph==0.2.65
pymysql==1.1.1
python-dotenv==1.0.1
weaviate==0.1.2
```

对单个依赖包安装：

- npm

  ```cmd
  npm install npm@latest -g
  ```

- python

  ```cmd
  python pip install Flask==3.1.0
  ```

### 安装

1. 在https://www.langchain.com/获取一个免费的 `API Key`

2. 克隆本仓库

   ```cmd
   git clone https://gitee.com/jinxsally/Storming.git
   ```

3. 安装 NPM 包

   ```
   npm install
   ```

4. 在`backend/.env`中填写`API KEY`

   ```cmd
   LANGCHAIN_API_KEY = '填写你的 API';
   ```

5. 配置数据库文件`models.py`

   ```python
   conn = pymysql.connect(
       host="localhost",
       user="root",
       passwd="xxx",
       port=3306,
       db="xxx",
       charset="utf8",
   )
   ```

6. `Docker`部署（确保本地存在`docker`）

   ```cmd
   docker-compose up -d
   ```
   
6. 使用以下命令运行（在`app`文件目录下）

   ```cmd
   python main.py
   ```

## 路线图

-  登录、注册
-  历史会话
-  世界观/知识点标签
-  个人中心
-  题目巩固

- 一键分享

## 贡献

贡献让开源社区成为了一个非常适合学习、启发和创新的地方。你所做出的任何贡献都是**受人尊敬**的。

如果你有好的建议，请复刻（fork）本仓库并且创建一个拉取请求（pull request）。你也可以简单地创建一个议题（issue），并且添加标签「enhancement」。不要忘记给项目点一个 star！再次感谢！

1. 复刻（Fork）本项目
2. 创建你的 Feature 分支 (`git checkout -b xxx`)
3. 提交你的变更 (`git commit -m 'xxx'`)
4. 推送到该分支 (`git push origin xxx`)
5. 创建一个拉取请求（`Pull Request`）

## 联系我们

hqg13550019896@163.com

## 致谢

助教：[**Qi-ming-Zhang**](https://github.com/Qi-ming-Zhang)、[**zhangjiarui530** ](https://github.com/zhangjiarui530)

指导老师：[**AliceCodeZhang**](https://github.com/AliceCodeZhang)

勤奋努力的队友：王菲、李涵一、李莲鑫

技术指导：王逸婷

