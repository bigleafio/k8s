FROM resin/rpi-raspbian:jessie-20170726

RUN groupadd -r couchdb && useradd -d /opt/couchdb -g couchdb couchdb

# Download dependencies
RUN apt-get update -y -qq && apt-get install -y --no-install-recommends \
    python python-pip \
 && pip install requests

COPY mem3_kube.py /opt/mem3_kube/

USER couchdb
WORKDIR /opt/mem3_kube

CMD ["mem3_kube.py"]
ENTRYPOINT ["/usr/bin/python"]
