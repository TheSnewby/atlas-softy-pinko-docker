FROM ubuntu:latest
LABEL maintainer="Stephen Newby <stephen.j.newby@gmail.com>"

ENV TZ=America/Chicago
ENV SHELL=/bin/bash
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Install dependencies and tools
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get clean
    # apt-get install -y sudo curl git python3 python3-pip mysql-server pkg-config && \
    # apt-get install -y libmysqlclient-dev libssl-dev libffi-dev

# Ensure MySQL can run as a service
# RUN mkdir -p /var/run/mysqld && chown -R mysql:mysql /var/run/mysqld

# # Install pip packages
# RUN pip3 install mysqlclient flasgger flask flask-cors flask-restful flask-sqlalchemy requests

# Expose the MySQL port
# EXPOSE 5000
# EXPOSE 5001

# # AirBnB Clone Environment Variables
# ENV HBNB_MYSQL_USER=hbnb_dev
# ENV HBNB_MYSQL_PWD=hbnb_dev_pwd
# ENV HBNB_MYSQL_HOST=localhost
# ENV HBNB_MYSQL_DB=hbnb_dev_db
# ENV HBNB_TYPE_STORAGE=db

CMD echo "Hello, World!"

# start the MySQL service
# CMD [ "service", "mysql", "start" ]

# command to create the volume
# docker volume create hbnb-dev

# command to build the image
# docker build -t hbnb-dev .

# command to run the container as a persistant dev environment without the volume
# docker run -it -p 5000:5000 -p 5001:5001 hbnb-dev:latest bash

# command to run the container as a persistant dev environment with the volume
# docker run -it -p 5000:5000 -p 5001:5001 -v hbnb-dev:/root hbnb-dev:latest bash

# start the MySQL service
# service mysql start