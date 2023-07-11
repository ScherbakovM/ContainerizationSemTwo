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


 
