FROM python:3.7-alpine
WORKDIR /root/composetest
RUN /usr/local/bin/python -m pip install --upgrade pip
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN apk add --no-cache mariadb-dev gcc python3-dev linux-headers musl-dev
RUN pip3 install mysqlclient
RUN pip3 install Flask-WTF
RUN pip3  install Flask-Login
RUN pip3 install redis
RUN pip3 install Flask-Mail
RUN pip3 install flake8
RUN pip3 install flask-debugtoolbar
RUN pip3 install gunicorn
RUN pip3 install  flask-redis
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN apk add --no-cache gcc musl-dev linux-headers 
COPY requirements.txt requirements.txt

RUN pip install -r requirements.txt
EXPOSE 5000
COPY . .
CMD ["flask", "run"]
