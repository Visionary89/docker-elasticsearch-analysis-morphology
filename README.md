# Elasticsearch with russian morphology support

* [imotov/elasticsearch-analysis-morphology](https://github.com/imotov/elasticsearch-analysis-morphology)
* [Official docker image from elasticseach](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)

##For simple use without x-pack security use this config: 
```yaml
version: "3.3"
services:
  elasticsearch:
    image: visionary89/elasticsearch-analysis-morphology:5.4.3
    volumes:
      - ./services_config/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml
    mem_limit: 1g
    ports:
      - 9200:9200
  kibana:
    image: docker.elastic.co/kibana/kibana:5.4.3
    ports:
      - 5601:5601
    volumes:
      - ./services_config/kibana.yml:/usr/share/kibana/config/kibana.yml
```