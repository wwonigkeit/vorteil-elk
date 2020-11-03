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
3. Download the Elasticsearch, Logstash and Kibana generic Linux distrubtions and extract to the root of the repository
4. Link the directories to the extracted generic Liux archives:

```$ ln -s elasticsearch-7.9.3 elasticsearch```
```$ ln -s logstash-7.9.3 logstash```
```$ ln -s kibana-7.9.3-linux-x86_64 kibana```

5. If you want to use NFS:
       
       - map the correct NFS shares (IP address & mount points) in the default.vcfg.nfs and rename to default.vcfg
       
       - copy the configuration files in /example_configs/* to the NFS share
   
   or, if you only want to use local disk:
       
       - rename default.vcfg.local to default.vcfg file
       
       - copy the configuration files in /example_configs/* to the /configs/* directory (or customise your own)
       
6. Run the machine using `vorteil run <cloned-directory>`

If you have any questions just ask!
