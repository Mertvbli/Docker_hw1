FROM python:3.9

COPY ./requirements.txt /src/requirements.txt

RUN pip3 install -r /src/requirements.txt

COPY . /src

WORKDIR src

RUN python3 manage.py migrate

CMD ["python3", "manage.py", "runserver", "0.0.0.0:80"]