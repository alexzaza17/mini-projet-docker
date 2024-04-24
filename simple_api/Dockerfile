FROM python:3.8-buster
MAINTAINER alexzaza17(bernardtapi1702@gmail.com)
RUN apt-get update -y && apt install python3-dev libsasl2-dev libldap2-dev libssl-dev -y
WORKDIR /
COPY  requirements.txt student_age.py /
RUN pip3 install -r requirements.txt
COPY /data
EXPOSE 5000
CMD ["python", "./student_age.py"]
