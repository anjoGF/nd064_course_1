## using a python base image
FROM python:2.7

LABEL maintainer='Anton Gordon'

# copy files from the host to the container
COPY . /app
#  defines the working directory within the container
WORKDIR /app
# run commands within the container.
# For example, invoke a pip command
# to install dependencies defined in the requirements.txt file.
RUN pip install -r requirements.txt

#exposing in port 3111
EXPOSE 3111

#initializing database
RUN python init_db.py

#Executing at the container start
CMD ["python", "app.py"]