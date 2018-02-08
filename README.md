Bro ELK Integration using Docker Compose
-----

Integration of [Bro](https://www.bro.org/) Network Security Monitor and [ELK](https://www.elastic.co/elk-stack) stack (i.e., Elasticsearch-Logstash-Kibana) using Docker Compose.

This is a simple integration based on the following open-source projects:

* [docker-elk](https://github.com/deviantony/docker-elk)
* [docker-bro](https://github.com/blacktop/docker-bro)

### Prerequisites
- [Docker](https://www.docker.com/community-edition#/download) version **1.10.0+**
- [Docker Compose](https://docs.docker.com/compose/install/) version **1.6.0+**

### Configuration 

Configure `bro` service in `docker-compose.yml` to listen to different network interface (default is `eth0`).

### Usage 

To run `docker-bro-elk`:

```bash
docker-compose up
```

or in detached mode:

```bash
docker-compose up -d
```

After running the services, you can access Kibana interface at `http://localhost:5601` and create new index pattern with prefix `logstash-*` to start exploring network data captured by Bro.


To stop `docker-bro-elk`, simply press `Ctrl+C` if running in foreground mode, or run the following command if running in detached mode:

```bash
docker-compose down
```
