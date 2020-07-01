### Creating Certificate for Xpack (Ubuntu 18.04)
Run any of below command in the Elasticsearch container to create the certificate 
```
/bin/elasticsearch-certutil ca      (or)
/bin/elasticsearch-certutil cert --ca elastic-stack-ca.p12
```
Copy the certfile file from the container to your locahost

```
docker cp containerid:/usr/share/elasticsearch/elastic-stack-ca.p12 .
```
### Run Elasticsearch & Kibana as docker containers
```
sudo sysctl -w vm.max_map_count=262144
docker-compose up -d
```
