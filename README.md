# ContainerizationSemTwo

### Контейнирезация семинар 2

 ### Команда для создания новой контрольной группы

``cgcreate -a $USER -g memory:mytestgroup -g cpu:mytestgroup`` 

 ``$USER`` // Текущий пользователь  
 ``-g memory:mytestgroup`` // ограничение на использование памяти  
 ``-g cpu:mytestgroup`` // ограничения на использование процессора  

 ### Каманда для проверки создания  контрольной группы 

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

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/0be80125-3f81-420f-ad81-2b396175ab63)

### Контейнер запущен и работает 

### Переходим к ограничению контейнера по памяти 

Открываем конфиг нашего контейнера командой

``nano /var/lib/lxc/test123/config``

 в __Container specific configuration__ дописываем строчку  
 
 ``lxc.cgroup2.memory.max = 256M``

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/fb4c9197-282a-4c03-bafb-4a2826384313)

__Сохраняем, выходим__



