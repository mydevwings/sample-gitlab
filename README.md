##Sample gitlab


Run it 
В директории с файлом **docker-compose.yml** 

Создать скрипт:

create_gitlab.sh

```
export GITLAB_HOME=/home/username/code/gitlab/data
docker-compose up -d 
```
Сделать скрипт выполняемым

chmod +x create_gitlab.sh

Пыполнить скрипт 
```
sh create_gitlab.sh 
```

### TODO 

отключить автостарт для gitlab



Подождать после некоторое время - gitlab может быть недоступен


По умолчанию localhost:9090

При первом запуске - будут просить задать пароль.
После задачи пароля - пользователь -  **admin@example.com**

### После - добавить своего пользователя


http://localhost:9090/admin/users

* CLick **new user** 
* Fill fields in **Accout**
* Return to users. Then edit created user and provide password

Login created user -change password if you need


* In snippet - for creating new project -  rename **hostname** to **localhost**
And yours port **9090**

from 
```
git remote add origin http://hostname/mydevwings/test.git
```

to

```
git remote add origin http://localhost:9090/mydevwings/test.git
```

### In project 

git config user.name "mydevwings" 
git config user.email "mydevwings@gmail.com"
