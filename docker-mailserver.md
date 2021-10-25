./Dockerfile:73:  curl https://packages.elasticsearch.org/GPG-KEY-elasticsearch | apt-key add - && \
./elk/Dockerfile:26:RUN /bin/grep -q  -F 'transport.host' /etc/elasticsearch/elasticsearch.yml || echo "transport.host: 127.0.0.1" >> /etc/elasticsearch/elasticsearch.yml
