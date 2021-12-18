## using a python base image
FROM python:2.7

LABEL maintainer='Anton Gordon'

## copy files to container place them in the app directory
COPY ./techtrends/requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY ./techtrends ./
COPY ./Dockerfile ./

## Initialize the database with the pre-defined posts in the init_db.py file
RUN python init_db.py

## Expose the application port 3111
EXPOSE 3111

## The application should execute at the container start
CMD ["python", "app.py"]