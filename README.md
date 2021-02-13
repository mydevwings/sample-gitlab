##Sample gitlab


### Создание 

В директории с файлом **docker-compose.yml** 

Создать скрипт:

**create_gitlab.sh**

```
export GITLAB_HOME=/home/username/code/gitlab/data
docker-compose up -d 
```

Сделать скрипт выполняемым


```
chmod +x create_gitlab.sh
```

Выполнить скрипт 

```
sh create_gitlab.sh 
```

Подождать после некоторое время 2-5 минуты- gitlab настраивается


По умолчанию localhost:9090

При первом запуске - будут просить задать пароль.
После задачи пароля - пользователь -  **admin@example.com** или **root**

### После - добавить своего пользователя


http://localhost:9090/admin/users

* CLick **new user** 
* Fill the fields in a **Accout** section
* Return to users. Then edit created user and provide password

Login created user -change password

* В docker-compose есть свойство **hostname**. Заполнить на свой нужный. Сейчас стоит **localhost** для запуска на своей машине локально.
* В снипетах по созданию проекта - добавить порт **9090**

from 
```
git remote add origin http://localhost/mydevwings/test.git
```

to

```
git remote add origin http://localhost:9090/mydevwings/test.git
```

### В проекте - добавить пользователя для gitlab - эти настройки локально для проекта

git config user.name "mydevwings" 
git config user.email "mydevwings@gmail.com"
