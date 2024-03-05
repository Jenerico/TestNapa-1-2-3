├── configure-webserver.yml  # Плейбук для настройки веб-сервера  
└── roles  

    ├── configure-firewall   # Роль для настройки фаерволла  
    │   ├── tasks  
    │   │   └── main.yml  
    │   └── vars  
    │         └── main.yml  
    ├── install-nginx        # Роль для установки Nginx  
    │   ├── defaults  
    │   │   └── main.yml  
    │   ├── handlers  
    │   │   └── main.yml  
    │   ├── tasks  
    │   │   └── main.yml  
    │   ├── templates  
    │   │   ├── nginx.service.j2  
    │   │   └── nginx  
    │   │       └── ... # Конфигурационные файлы Nginx  
    │   └── vars  
    │       └── main.yml  
    └── prepare-disk         # Роль для подготовки диска  
        ├── tasks  
        │   └── main.yml  
        └── vars  
            └── main.yml  
