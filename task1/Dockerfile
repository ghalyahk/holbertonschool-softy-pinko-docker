FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

# fix externally managed error (مهم)
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED || true

RUN pip3 install flask

WORKDIR /app

COPY api.py /app/api.py

CMD ["python3", "api.py"]
