Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:Vladimir-spb/yacut.git
```

```
cd yacut
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

* Если у вас Linux/macOS

    ```
    source venv/bin/activate
    ```

* Если у вас windows

    ```
    source venv/scripts/activate
    ```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Запуск:

Создать файл .env с данными:

FLASK_APP=yacut
FLASK_ENV=development
DATABASE_URI= по умолчанию "sqlite:///db.sqlite3"
SECRET_KEY="секретный код" по умолчанию "12345"

Применить миграции
```
flask db upgrade
```
Запустить сервер
```
flask run
```
проект доступен по http://localhost:5000/

# Rest API 

/api/id/ — POST-запрос на создание новой короткой ссылки;
/api/id/<short_id>/ — GET-запрос на получение оригинальной ссылки по указанному короткому идентификатору.

Автор 
Коршак Владимир Юрьевич