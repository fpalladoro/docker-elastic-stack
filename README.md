# docker-elastic-stack

Docker swarm compose project ready to launch an Elastic stack (Elasticsearch, Kibana, Logstash and Metricbeat)


## Requirements

* `docker-engine` >= 1.13
* Docker swarm mode


## Launch stack

```
docker stack deploy -c stack.yml elstack
docker service update  --publish-add 5601:5601 elstack_kibana
```


## ToDo

- [x] Add persistent volumes to elasticsearch and kibana
- [ ] Include kibana published port on [compose file](stack.yml)
