## CurrencyAggregator
A code that allows you to transfer currency.

## How to run:
Step one, install dependencies:
```sh
pip install -r requirements.txt
```
Apply migration:
```sh
python manage.py migrate
```
Run broker:
```sh
docker run -d -p 5672:5672 rabbitmq
```
Run celery beat:
```sh
celery -A hilel12 beat
```
Run worker:
```sh
celery -A hilel12 worker -l INFO


or on Windows:
1. pip install eventlet
2. celery -A hilel12 worker -l INFO -P eventlet
```
Run server:
```sh
python manage.py runserver  
or 
python3 manage.py runserver
```
