Структура проекта
```
├── configure-server.yml
└── roles
    ├── add-user
    │   ├── files
    │   │   └── testuser.pub       # Сюда поместите сгенерированный публичный SSH ключ
    │   ├── tasks
    │   │   └── main.yml           # Задачи для создания пользователя и настройки доступа
    │   └── templates
    │       └── sudoers.d_testuser.j2  # Шаблон для настройки sudo без пароля
    └── deploy-bin
        ├── files
        │   ├── app.conf          # Файл конфигурации приложения
        │   ├── multisocket.bin   # Бинарный файл для многоядерных систем
        │   ├── singlesocket.bin  # Бинарный файл для одноядерных систем
        │   └── web.conf          # Файл конфигурации веб-сервера
        └── tasks
            └── main.yml          # Задачи для развертывания файлов и настройки системы
```
Для запуска плейбука
```bash
ansible-playbook -i <путь_к_инвентарному_файлу> configure-server.yml
