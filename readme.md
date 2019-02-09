
## 生产环境部署

```bash
# 安装虚环境
pip install virtualenv

# 使用虚环境为应用创建虚拟环境
# 在工程中分建立一个venv目录，该目录中复制了一份完整的当前系统的Python环境
virtualenv venv

# 指定虚拟环境
# 后面的安装与执行的Python命令都会在这个目录下进行
source ./venv/bin/activate

# 安装项目依赖
pip install -r requirements.txt

# 生成数据库迁移文件
python manage.py makemigrations

# 数据库迁移，写入数据库
python manage.py migrate

# 启动项目
nohup python manage.py runserver & disown
```


## Author 作者

[ninemill.song - 九毫](https://github.com/ninemilli-song)

### 许可（License）

Copyright (c) [ninemilli.song](https://github.com/ninemilli-song)

[MIT License][MIT]

[MIT]: ./LICENSE "Mit License"
