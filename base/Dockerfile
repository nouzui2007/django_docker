FROM python:3

ENV PYTHONUNBUFFERED 1
ENV APP_PATH /opt/apps

RUN mkdir $APP_PATH

ADD requirements.txt $APP_PATH
ADD . $APP_PATH
WORKDIR $APP_PATH

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

EXPOSE 8000:8000
