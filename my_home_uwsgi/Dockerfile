# default
#FROM python:3

# for arm32 system
FROM arm32v7/python:3.6.4-jessie

RUN apt-get update

WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

EXPOSE 29000
CMD ["uwsgi", "--ini", "my_home/uwsgi.ini"]
