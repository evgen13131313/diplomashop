OnlineSale
OnlineSale — это веб-приложение для интернет-магазина, разработанное на фреймворке Django. Проект предоставляет базовый функционал для онлайн-торговли, включая каталог товаров, систему аутентификации пользователей и административную панель для управления ассортиментом.
Системные требования: Python (3.8|3.10+) Django (4.0|4.2+) SQLite (3.0+|3.35+) Pillow (9.0|10.1.0) Браузер (chrome)
Инструкция по установке Шаг 1: Скачайте проект (git clone https://github.com/your-username/DiplomaShop.git, cd DiplomaShop) Шаг 2: Создайте виртуальное окружение (python -m venv venv, venv\Scripts\activate) Шаг 3: Установите зависимости (pip install --upgrade pip, pip install -r requirements.txt)  Шаг 4: Примените миграции (python manage.py makemigrations, python manage.py migrate) Шаг 5: Создайте суперпользователя (администратора) (python manage.py createsuperuser) Шаг 6: Создайте необходимые папки (mkdir static, mkdir static\css, mkdir static\img, mkdir media, mkdir media\products)
Инструкция по запуску Активируйте виртуальное окружение: (venv\Scripts\activate ) Запустите сервер разработки: (python manage.py runserver) Откройте браузер и перейдите: (Главная http://127.0.0.1:8000/) (Админ-панель http://127.0.0.1:8000/admin/) (Регистрация http://127.0.0.1:8000/register/) (Вход http://127.0.0.1:8000/login/)      Зайдите в админ-панель: http://127.0.0.1:8000/admin/  Войдите под суперпользователем(логин: Admin, пароль 123) Создайте категории товаров (раздел "Категории") Добавьте товары (раздел "Товары") Проверьте отображение на главной странице
iplomaShop/
│
├── 📂 config/                    # Настройки проекта Django
│   ├── __init__.py
│   ├── settings.py               # Основные настройки проекта
│   ├── urls.py                   # Главная маршрутизация
│   ├── asgi.py                   # ASGI конфигурация
│   └── wsgi.py                   # WSGI конфигурация
│
├── 📂 shop/                      # Основное приложение магазина
│   ├── migrations/               # Миграции базы данных
│   │   └── __init__.py
│   ├── templates/
│   │   └── shop/                 # HTML шаблоны
│   │       ├── base.html         # Базовый шаблон
│   │       ├── index.html        # Главная страница
│   │       ├── login.html        # Страница входа
│   │       ├── register.html     # Страница регистрации
│   │       └── profile.html      # Личный кабинет
│   ├── __init__.py
│   ├── admin.py                  # Настройки админ-панели
│   ├── apps.py                   # Конфигурация приложения
│   ├── forms.py                  # Формы (регистрация, вход)
│   ├── models.py                 # Модели данных (БД)
│   ├── urls.py                   # Маршруты приложения
│   └── views.py                  # Обработчики запросов
│
├── 📂 static/                    # Статические файлы
│   ├── css/
│   │   └── style.css             # Основные стили
│   └── img/
│       └── logo.png              # Логотип сайта
│
├── 📂 media/                     # Пользовательские файлы
│   └── products/                 # Изображения товаров
│
├── 📂 venv/                      # Виртуальное окружение Python
│
├── .gitignore                    # Игнорируемые файлы Git
├── db.sqlite3                    # База данных SQLite
├── manage.py                     # Утилита управления Django
├── requirements.txt              # Зависимости проекта
└── README.md                     # Этот файл
