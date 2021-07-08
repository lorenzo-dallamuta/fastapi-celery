# Asynchronous Tasks with FastAPI and Celery

Example of how to handle background processes with FastAPI, Celery, and Docker.

### Quick Start

Spin up the containers:

```sh
#$ docker-compose up -d --build
$ docker-compose up -d --build --scale worker=3
$ docker-compose exec web python -m pytest -k "test_task and not test_home"
$ docker-compose exec web python -m pytest -k "test_task_status"
```

Open your browser to [http://localhost:8004](http://localhost:8004)
Open your browser to [http://localhost:5556/](http://localhost:5556/)


### Hack for typing-extensions (21/07/08)

pipenv install -r project/requirements.txt
delete Pipfile.lock
pipenv lock
pipenv install

for some reason the first time around the 
typing-extensions dependency gets a 
python < 3.8 marker even if it's not true