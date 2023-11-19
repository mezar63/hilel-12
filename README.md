# hilel-12
CurrencyAggregator
How to run:
Step one, install dependencies:
 pip install -r requirements.txt
Apply migration:
python manage.py migrate
Run broker:
docker run -d -p 5672:5672 rabbitmq
Run celery beat:
celery -A hilel12 beat 
Run worker:
celery -A hilel12 worker -l INFO

or on Windows:
1. pip install eventlet
2. celery -A hilel12 worker -l INFO -P eventlet
Run server:
python manage.py runserver  
or 
python3 manage.py runserver  
