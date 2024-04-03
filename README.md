# Learning log
*基于 Django 实现的在线日志系统*

## 快速上手 🤗
### 本地构建
- 克隆仓库
```shell
cd learning_log
git clone git@github.com:rhee2333/learning_log.git
```
- 创建Anaconda环境
```shell
conda create -n ll_env python=3.11
```
- 安装依赖
```shell
# 依赖包明细请查看requirements.txt
conda activate ll_env
conda install conda-forge::django
conda install conda-forge::django-bootstrap5
```

- 在Django中创建项目并执行前期准备
```shell
cd learning_log
django-admin startproject ll_project .
ls .\ll_project
# 初始化数据库
python .\manage.py migrate
```

- 运行项目
```shell
python .\manage.py runserver
```
---
### ***以下内容为从零搭建系统，不感兴趣可忽略***

- 创建应用程序
```shell
# 新建learning_log应用
python .\manage.py startapp learning_logs
# 新建accounts应用
python .\manage.pystartapp accounts
# 新建应用存储数据授权(model.py变更需运行)
python .\manage.py makemigrations {app_name}
python .\manage.py migrate
```

- 创建管理员用户
```shell
python .\manage.py createsuperuser
# eg: username: admin passwd: admin
```
