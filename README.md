# hbg-dbdev
Providing an Image to demonstrate elasticsearch in addtion to MariaDB

## Based on hgb-phpdev

- Look at [hgb-phpdev](https://github.com/Digital-Media/hgb-phpdev) for **Installation**, **Troubleshooting** and **Usage**.
- Remember, that we use ``hgb-dbdev`` instead of ``hgb-phpdev`` and replace this path name where necessary.

## Additional technologies and requirements

* [ElasticSearch 6.3.1](https://www.elastic.co/guide/en/elasticsearch/reference/6.3/install-elasticsearch.html)
* [Oracle JRE SE](https://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [German Word Decompounder](https://github.com/uschindler/german-decompounder)
* [Redis 4.0](https://redis.io/)
* [Neo4J](https://neo4j.com)

## Start and stop scripts for ElasticSearch (may take 20-30 seconds)

* ``startES.sh`` starts ElasticSearch in background
```
    netstat -apnt
    (Not all processes could be identified, non-owned process info
     will not be shown, you would have to be root to see it all.)
    Active Internet connections (servers and established)
    Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
    tcp        0      0 127.0.0.1:3306          0.0.0.0:*               LISTEN      -
    tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      -
    tcp        0     36 10.0.2.15:22            10.0.2.2:55186          ESTABLISHED -
    tcp6       0      0 127.0.0.1:9200          :::*                    LISTEN      2036/java
    tcp6       0      0 ::1:9200                :::*                    LISTEN      2036/java
    tcp6       0      0 :::80                   :::*                    LISTEN      -
    tcp6       0      0 127.0.0.1:9300          :::*                    LISTEN      2036/java
    tcp6       0      0 ::1:9300                :::*                    LISTEN      2036/java
    tcp6       0      0 :::22                   :::*                    LISTEN      -
    tcp6       0      0 :::443                  :::*                    LISTEN      -
```

* ``stopES.sh`` stops ElasticSearch, when started in background

```
    netstat -apnt
    (Not all processes could be identified, non-owned process info
     will not be shown, you would have to be root to see it all.)
    Active Internet connections (servers and established)
    Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
    tcp        0      0 127.0.0.1:3306          0.0.0.0:*               LISTEN      -
    tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      -
    tcp        0      0 10.0.2.15:22            10.0.2.2:55186          ESTABLISHED -
    tcp6       0      0 :::80                   :::*                    LISTEN      -
    tcp6       0      0 :::22                   :::*                    LISTEN      -
    tcp6       0      0 :::443                  :::*                    LISTEN      -
```
