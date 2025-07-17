# TODO
# Django TODO приложение

Простое веб-приложение для управления задачами, созданное на Django.

## Описание проекта

Проект реализует базовый функционал для работы с задачами (CRUD операции) через Django ORM.

## Установка и настройка

1. Клонируйте репозиторий:
```bash
git clone https://github.com/89245095129/TODO.git
cd TODO

Создайте и активируйте виртуальное окружение:

bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

Установите зависимости:

bash
pip install django
Примените миграции:

bash
python manage.py migrate

Создайте суперпользователя:

bash
python manage.py createsuperuser
Запустите сервер:

bash
python manage.py runserver

Структура проекта:

django/
├── config/             # Основной проект Django
├── todo/               # Приложение для работы с задачами
│   ├── models.py       # Модель Task
│   ├── views.py        # Представления
│   └── urls.py         # Маршруты приложения
├── manage.py           # Утилита управления
└── README.md           # Этот файл

Реализованные задачи

Задача 1. Создание приложения
Создан проект Django (config)

Добавлено приложение todo

Настроены базовые маршруты

Приложение подключено в INSTALLED_APPS

Задача 2. Модель Task
Модель содержит поля:

title - заголовок задачи (CharField)

description - описание (TextField)

completed - статус выполнения (BooleanField)

created_at - дата создания (DateTimeField)

Миграции созданы и применены:

bash
python manage.py makemigrations
python manage.py migrate

Задача 3. Работа с данными
Реализованы CRUD операции через Django ORM:

python
# Создание
Task.objects.create(title="Задача", description="Описание")

# Чтение
tasks = Task.objects.all()

# Обновление
task = Task.objects.get(id=1)
task.completed = True
task.save()

# Удаление
task.delete()
Административная панель
Доступна по адресу /admin после создания суперпользователя.

Лицензия
MIT
