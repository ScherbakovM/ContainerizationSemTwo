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

### Создаём новый Linux Container 

``lxc-create -n test123 -t ubuntu ``

Если команда не запускается возможнго потребуется установить пакет с зависимостями для lxc 

``apt-get install lxc-templates``

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/ab061a47-40ac-44b4-a3ec-a9cf4f7fd1a4)



### Дожидаёмся сообщения об успешной установке

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/64991f10-f742-40cf-be58-4e2be9bdf941)


### Переходим к запуску контейнера
 
``lxc-start -n test123`` // запуск контейнера  
``lxc-attach -n test123`` // вход в контейнер  

