# ContainerizationSemTwo

### Контейнирезация семинар 2

 ## Команда для создания новой контрольной группы

``cgcreate -a $USER -g memory:mytestgroup -g cpu:mytestgroup`` 

 ``$USER`` // Текущий пользователь  
 ``-g memory:mytestgroup`` // ограничение на использование памяти  
 ``-g cpu:mytestgroup`` // ограничения на использование процессора  

 ## Каманда для проверки создания  контрольной группы 

 ``ls /sys/fs/cgroup/mytestgroup/``

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/52c0ad6c-b4c7-4112-8ec7-1998bd08f88e)

### Создаём новый контейнер 

``lxc-create -n test123 -t ubuntu ``

Если команда не запускается возможнго потребуется установить пакет с зависимостями для lxc 

``apt-get install lxc-templates``

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/221e2624-71da-498b-9904-ed0a7049461d)


### Дожидаёмся сообщения об успешной устанвки 

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/acc18d74-18d8-4924-bd93-c2da8c2b2a3a)


### Переходим к запуску контейнера
 
``lxc-start -n test123`` // запуск контейнера  
``lxc-attach -n test123`` // вход в контейнер  

