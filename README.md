# vorteil-elk

A simple implementation of [ElasticSearch](https://www.elastic.co/elasticsearch/), [Logstash](https://www.elastic.co/logstash/) & [Kibana](https://www.elastic.co/kibana/)

## Description

This is the public repo used to create the Medium article:

https://medium.com/@wilhelm-wonigkeit/an-elk-stack-without-an-os-9d01a1761d8d

This package contains the Vorteil configuration files, libraries and some configuration files neeed for the ELK stack. The binaries themselves should be downloaded using the following commmands:

ElasticSearch:

```wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.9.3-linux-x86_64.tar.gz```

Logstash:

```wget https://artifacts.elastic.co/downloads/logstash/logstash-7.9.3.tar.gz```

Kibana:

```wget https://artifacts.elastic.co/downloads/kibana/kibana-7.9.3-linux-x86_64.tar.gz```


## Using the Vorteil machine configuration

1. Download and install the latest [Vorteil open source toolkit](https://github.com/vorteil/vorteil)
2. Clone the repo to an appropriate directory on your local machine
3. Run the machine using `vorteil run <cloned-directory>`
4. Get the k3s.yaml file to configure kubectl connections `curl localhost:8080 -o k3s.yaml`
5. Verify access using `./kubectl --kubeconfig k3s.yaml get pods --namespace=kube-system`

If you have any questions just ask!
