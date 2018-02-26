
# Overview of Elasticsearch

When it comes to databases, we usually think of [MySQL](https://www.mysql.com/), [PostgreSQL](https://www.postgresql.org/), and the distributed DBMS such as [MongoDB](https://www.mongodb.com/). There is the figure below which refers to the [DB-Engines Ranking](https://db-engines.com/en/ranking) and reflects the popularity of major databases in recent years.

![DB-Engines Ranking Table (Feb, 2018)](https://cdn-images-1.medium.com/max/2000/1*Wx7cA9OWPFazaCCuF72fTA.png)*DB-Engines Ranking Table (Feb, 2018)*

Today, we will talk about the search engine which reached the top ten databases in this year’s breakthrough - [**Elasticsearch](https://www.elastic.co)**.

![DB-Engines Ranking Chart (Feb, 2018)](https://cdn-images-1.medium.com/max/2000/1*RrKMZXY9pRvdv4phlOo4Mw.png)*DB-Engines Ranking Chart (Feb, 2018)*

## Advantage

### Elasticsearch is a **distributed** store, search and analytics engine capable of solving a growing number of use cases.

1. ES provides the cluster which is a collection of one or more nodes (servers) to hold your entire data and provide federated indexing and search capabilities across all nodes. Therefore, it can easily achieve scaling out your search volume.

1. ES provides the ability to subdivide your index into multiple pieces called shards. When you create an index, you can simply define the number of shards that you want. Each shard is in itself a fully-functional and independent “index” that can be hosted on any node in the cluster.

1. ES is a near real time search platform. What this means is there is a slight latency (normally one second) from the time you index a document until the time it becomes searchable.

### Using RESTful for communication, familiar to mainstream developers, intuitive interface, most languages are supported.

### The core of Elasticsearch is built on top of Apache Lucene, is a well-known, open source, full-text search-engine library. However, Elasticsearch is much more than just Lucene and much more than “just” full-text search. It can also be described as follows:

1. A distributed real-time document store where *every field* is indexed and searchable.

1. A distributed search engine with real-time analytics.

1. Capable of scaling to hundreds of servers and petabytes of structured and unstructured data

## Weak points

* Not support scheduling.

* Have a little delay in reading and writing.

* Not support permission management.

## Use cases

* Wikipedia uses Elasticsearch to provide ***full-text search*** with highlighted search snippets, and ***search-as-you-type*** and ***did-you-mean*** suggestions.

* *The Guardian* uses Elasticsearch to combine **visitor logs** with **social -network data** to provide real-time feedback to its editors about the public’s response to new articles.

* Stack Overflow combines **full-text search** with **geolocation queries** and uses ***more-like-this*** to find related questions and answers.

* GitHub uses Elasticsearch to query 130 billion lines of code.

* SoundCloud: Use Elasticsearch to intelligently search and deliver content to tens of millions.

* Baidu: Baidu currently uses ES for analysis. It collects all kinds of index data and user-defined data on all servers in Baidu. Through multi-dimensional analysis and display of various data, it assists in positioning an exception or business exception. At present, it covers more than 20 business lines within Baidu, up to 100 machines in a single cluster and 200 ES nodes, importing 30TB+ daily data .

## Comparison

    +--------+----------+------------+
    |   ES   |   SQL    |  MongoDB   |
    +--------+----------+------------+
    | Index  | Database | Database   |
    | Shard  | Shard    | Shard      |
    | Type   | Table    | Collection |
    | Field  | Column   | Field      |
    | Object | Record   | Record     |
    +--------+----------+------------+

## Conclusion

In the era of big data, it often encounters billions of data and real-time search, so that we have NoSQL. However, it’s still not enough in real world, you may be find the “needle in the haystack“ for billions of data. When full-text search, structured search, and analysis become the necessary requirements, this will be the best condition to use Elasticsearch. It saves on the learning costs of understanding Lucene’s complex operating principles and communicates with the RESTful API behind the open-source community and experience. I believe Elasticsearch will be keeping in the top 10 popular database for a while.
