==========================================
印度手机用户行为可视化大屏
Visualization Dashboard of Indian Mobile Phone Users' Behavior
==========================================

📚 项目简介
📚 Project Introduction
本项目主要对印度手机用户进行行为分析，对手机用户行为数据（包括年龄、性别、屏幕时间、数据使用量、应用使用情况等）做可视化处理，并选择用户的消费行为开展k-means聚类分析。
This project mainly conducts behavioral analysis on Indian mobile phone users, performs visualization processing on mobile phone users' behavioral data (including age, gender, screen time, data usage, app usage, etc.), and selects users' consumption behaviors for k-means clustering analysis.

------------------------------------------
### 数据来源
### Data Source
本文采用的原始数据集来自kaggle公开的数据集，共包含17686条记录。该数据集涵盖16个字段，具体各字段名称及其含义如下：
The original dataset used in this paper is from the public dataset on Kaggle, with a total of 17,686 records. The dataset includes 16 fields, and the names and meanings of each field are as follows:

字段名                     字段含义                     Field Name                     Field Meaning
User ID                   用户唯一标识符               User ID                       Unique user identifier
Age                       用户年龄                     Age                           User's age
Gender                    用户性别                     Gender                        User's gender
Location                  用户所在城市                 Location                      User's city of residence
Phone Brand               用户使用的手机品牌           Phone Brand                   Brand of mobile phone used by the user
OS                        用户手机的操作系统           OS                            Operating system of the user's mobile phone
Screen Time (hrs/day)     用户每天使用手机屏幕的总时间（小时） Screen Time (hrs/day)       Total daily mobile phone screen time of the user (hours)
Data Usage (GB/month)     用户每月使用的移动数据量（GB） Data Usage (GB/month)         Monthly mobile data usage of the user (GB)
Calls Duration (min/day)  用户每天通话的总时长（分钟）   Calls Duration (min/day)      Total daily call duration of the user (minutes)
Number of Apps Installed  用户手机上安装的应用程序数量 Number of Apps Installed      Number of applications installed on the user's mobile phone
Social Media Time (hrs/day) 用户每天在社交媒体上花费的时间（小时） Social Media Time (hrs/day) Daily time spent by the user on social media (hours)
E-commerce Spend(INR/month) 用户每月在电子商务平台上的消费金额（印度卢比） E-commerce Spend(INR/month) Monthly consumption amount of the user on e-commerce platforms (Indian Rupee)
Streaming Time (hrs/day)  用户每天在流媒体平台（如视频、音乐）上花费的时间（小时） Streaming Time (hrs/day) Daily time spent by the user on streaming platforms (e.g., videos, music) (hours)
Gaming Time (hrs/day)     用户每天在手机游戏上花费的时间（小时） Gaming Time (hrs/day)       Daily time spent by the user on mobile games (hours)
Monthly Recharge Cost (INR) 用户每月为手机充值或支付套餐费用的金额（印度卢比） Monthly Recharge Cost (INR) Monthly amount recharged or paid for mobile phone plans by the user (Indian Rupee)
Primary Use               用户使用手机的主要用途       Primary Use                   Main purpose of the user's mobile phone usage

------------------------------------------
🎯 研究目标
🎯 Research Objectives
本研究通过用户与智能手机交互多维度数据整合与动态分析，旨在揭示用户行为的内在逻辑，并为数字时代的商业创新与社会治理提供科学依据。
Through the integration and dynamic analysis of multi-dimensional data on users' interaction with smartphones, this study aims to reveal the inherent logic of user behavior and provide a scientific basis for commercial innovation and social governance in the digital age.

------------------------------------------
📁 项目结构
📁 Project Structure
keshihuapingtai/
├── src/                     # 源代码 | Original code
│   ├── app.py               # 启动可视化大屏服务（访问对应网址） | Start visualization dashboard service (access the corresponding URL)
│   ├── ciyun.py             # 生成词云 | Generate word cloud
│   ├── data_processing.py   # 生成饼图、玫瑰图、热力图 | Generate pie charts, rose charts, heatmaps
│   ├── k-means.py           # k-means聚类分析 | k-means clustering analysis
│   ├── map.py               # 生成地图可视化 | Generate map visualization
│   └── map1.py              # 生成地图HTML文件 | Generate map HTML file
├── static/                  # 静态资源 | Static resources
│   ├── css/                 # CSS样式文件 | CSS style files
│   │   ├── style.css
│   │   └── app.css
│   ├── data/                # 源数据文件 | Source data files
│   │   └── phone_india.csv
│   ├── img/                 # 生成的可视化图片 | Generated visualization images
│   └── favicon.ico          # 网站图标 | Website favicon
├── templates/               # HTML模板文件 | HTML template files
│   └── index.html           # 大屏首页HTML | Dashboard homepage HTML
└── README.md                # 项目说明文档 | Project documentation

------------------------------------------
🔧 环境配置
🔧 Environment Configuration
### 基础依赖版本要求
### Basic Dependency Version Requirements
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
scikit-learn>=1.2.0
streamlit>=1.20.0

### 完整依赖包列表
### Complete Dependencies List
- Python 版本：3.8+ | Python Version: 3.8+
- pandas
- numpy
- scipy
- matplotlib
- seaborn
- scikit-learn
- geopandas
- shapely
- networkx
- wordcloud
- flask
- KMeans
- os
- csv
- silhouette_score
- StandardScaler

------------------------------------------
📁 使用方法
📁 Usage
### 1. 生成各类分析图表
### 1. Generate Various Analysis Charts
运行以下脚本，生成对应的数据分析可视化图表：
Run the following scripts to generate corresponding data analysis and visualization charts:
python src/ciyun.py
python src/data_processing.py
python src/k-means.py
python src/map.py
python src/map1.py

### 2. 启动可视化大屏
### 2. Launch Visualization Dashboard
运行app.py脚本启动服务，访问输出的网址即可查看可视化大屏：
Run the app.py script to start the service, and access the output URL to view the visualization dashboard:
python src/app.py

------------------------------------------
💡 未来工作
💡 Future Work
- 选择更多字段进行数据分析 | Select more fields for data analysis
- 选择更多的字段进行聚类 | Select more fields for clustering
- 连接本地数据库 | Connect to local database

------------------------------------------
👥 团队成员
👥 Team Members
- [何俊辉] (2501212913) | [He Junhui] (2501212913)
- [张骋旭] (2501212936) | [Zhang Chengxu] (2501212936)
- [陆胤] (2501212930) | [Lu Yin] (2501212930)
- [陈安杰] (2501112421) | [Chen Anjie] (2501112421)
