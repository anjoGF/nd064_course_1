## using a python base image
FROM python:2.7

LABEL maintainer='Anton Gordon'

## copy files to container place them in the app directory
COPY . /app

## set the working directory
WORKDIR /app

## install the dependencies from requirements.txt file
RUN pip install -r requirements.txt

## Initialize the database with the pre-defined posts in the init_db.py file
RUN python init_db.py

## Expose the application port 3111
EXPOSE 3111

## The application should execute at the container start
CMD ["python", "app.py"]