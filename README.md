# eka
Quickly run Elasticsearch, Kibana and APM Server locally with Docker Compose.

## Usage

```
docker-compose up
```

This will start:
- a single-node Elasticsearch (v7.10) cluster running on http://localhost:9200 on your machine (no authentication)
- a Kibana (v7.10) instance running on http://localhost:5601 on your machine (no authentication)
- an APM Server (v7.10) instance running on http://localhost:8200 on your machine (no authentication)

It should take only a few minutes to setup on the first run. Visit Kibana on http://localhost:5601 and enjoy! You can also visit http://localhost:8200 to verify that APM Server is up (you should get a JSON response containing the instance details).


You can pass the name of the service(s) to run if you don't want to run all services:

```
docker-compose up elasticsearch kibana
```

## Configuring stuff
You can configure a number of things (like authentication) via environment variables, or by mounting a config file as a volume. See the Elastic docs:
- [Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)
- [Kibana](https://www.elastic.co/guide/en/kibana/current/docker.html)
- [APM Server](https://www.elastic.co/guide/en/apm/server/current/running-on-docker.html)
- [The whole Elastic Stack](https://www.elastic.co/guide/en/elastic-stack-get-started/current/get-started-docker.html)

Looking for a way to run the Elastic stack in production? Yeah, you shouldn't use this. See the docs linked above for tips on that.
