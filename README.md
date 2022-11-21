<br>

<p align="center">
     <img src="https://age.apache.org/age-manual/master/_static/logo.png" width="30%" height="30%">
</p>
<br>

<h3 align="center">
    <a href="https://age.apache.org/age-manual/master/_static/logo.png" target="_blank">
        <img src="https://age.apache.org/age-manual/master/_static/logo.png"" height="25" height="30% alt="Apache AGE">
    </a>
    <a href="https://age.apache.org/age-manual/master/_static/logo.png" target="_blank">
    </a>
     is the leading multi-model graph database </h3>
     
</h3>

<h3 align="center">Graph Processing & Analytics for Relational Databases</h3>

<br>


</br>



<p align="center">                                                                                                    
  <a href="https://github.com/apache/age/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/apache/age"/>
  </a>
  &nbsp;
  <a href="https://github.com/apache/age/releases">
    <img src="https://img.shields.io/badge/Release-v1.1.0-FFA500?labelColor=gray&style=flat&link=https://github.com/apache/age/releases"/>
  </a>
  &nbsp;
  <a href="https://github.com/apache/age/issues">
    <img src="https://img.shields.io/github/issues/apache/age"/>
  </a>
  &nbsp;
  <a href="https://github.com/apache/age/network/members">
    <img src="https://img.shields.io/github/forks/apache/age"/>
  </a>
  &nbsp;
  <a href="https://github.com/apache/age/stargazers">
    <img src="https://img.shields.io/github/stars/apache/age"/>
  </a>
  &nbsp;
  <a href="https://discord.gg/NMsBs9X8Ss">
    <img src="https://img.shields.io/discord/1022177873127280680.svg?label=discord&style=flat&color=5a66f6"></a>
</p>

<br>


<h2><img height="20" src="/img/AGE.png">&nbsp;&nbsp;What is Apache AGE?</h2>

[Apache AGE](https://age.apache.org/#) is an extension for PostgreSQL that enables users to leverage a graph database on top of the existing relational databases. AGE is an acronym for A Graph Extension and is inspired by Bitnine's AgensGraph, a multi-model database fork of PostgreSQL. The basic principle of the project is to create a single storage that handles both the relational and graph data model so that the users can use the standard ANSI SQL along with openCypher, one of the most popular graph query languages today. 

Since AGE is based on the powerful PostgreSQL RDBMS, it is robust and fully featured. AGE is optimized for handling complex connected graph data. It provides plenty of robust databases features essential to the database environment, including ACID transactions, multi-version concurrency control (MVCC), stored procedure, triggers, constraints, sophisticated monitoring, and a flexible data model (JSON). Users with a relational background who require graph data analytics can use this extension with minimal effort because they can use existing data without having to go through migration. 

There is a strong need for cohesive, easy-to-implement multi-model databases. As an extension of PostgreSQL, AGE supports all the functionalities and features of PostgreSQL while also offering a graph model to boot.

<h2><img height="20" src="/img/tick.svg">&nbsp;&nbsp;Overview</h2>

Apache AGE is : 

- **Powerful**: adds graph database support to the already popular PostgreSQL database: PostgreSQL is used by organizations including Apple, Spotify, and NASA.
- **Flexible**: allows you to perform openCypher queries, which makes complex queries much easier to write. It also enables multiple graphs at the same time.
- **Intelligent**: allows you to perform graph queries that are the basis for many next-level web services such as fraud detection, master data management, product recommendations, identity and relationship management, experience personalization, knowledge management, and more.


<h2><img height="20" src="/img/features.svg">&nbsp;&nbsp;Features</h2>

- **Cypher Query**: supported graph query language
- **Hybrid Querying**: enable SQL and/or Cypher
- **Querying**: enable multiple graphs
- **Hierarchical**: graph label organization
- **Property Indexes**: on both vertices(nodes) and edges
- **Full PostgreSQL**: supports PG features


![Database, gdb, and fast](/img/hybrid.png)
![Database, gdb, and fast](/img/gdb.png)
![Database, gdb, and fast](/img/fast.png)
![Database, gdb, and fast](/img/gviz.png)


<h2><img height="20" src="/img/documentation.svg">&nbsp;&nbsp;Documentation</h2>

Refer to our latest [Apache AGE documentation](https://age.apache.org/age-manual/master/index.html) to learn about installation, features, built-in functions, and  Cypher queries.



<h2><img height="20" src="/img/installation.svg">&nbsp;&nbsp;Pre-Installation</h2>

Install the following essential libraries according to each OS. Building AGE from the source depends on the following Linux libraries (Ubuntu package names shown below):

- **CentOS**
```bash
yum install gcc glibc glib-common readline readline-devel zlib zlib-devel flex bison
```
- **Fedora**
```bash
dnf install gcc glibc bison flex readline readline-devel zlib zlib-devel
```
- **Ubuntu**
```bash
sudo apt-get install build-essential libreadline-dev zlib1g-dev flex bison
```

<h2><img height="20" src="/img/installation.svg">&nbsp;&nbsp;Installation</h2>

Apache AGE is intended to be simple to install and run, requiring only one command from your terminal. Apache AGE can be installed with Docker and the traditional ways. 

<h4><a href="https://surrealdb.com/install#gh-dark-mode-only"><img width="20" src="/img/pg.svg"></a>
&nbsp;Install PosgtreSQL
</h4>

You will need to install an AGE-compatible version of Postgres for Postgres 12.

```bash
sudo apt install postgresql-12
```


<h4><img width="20" src="/img/installation.svg"> 

&nbsp;Install AGE 
</h4>



```bash
pg_config
```
```bash
make install
```
```bash
make PG_CONFIG=/path/to/postgres/bin/pg_config install
```


<h4></a><img width="20" src="/img/docker.svg"></a>
&nbsp;Run using Docker
</h4>

<h5> Get the docker image </h5>

```bash
docker pull apache/age

```
<h5> Create AGE docker container </h5>

```bash
docker run \
    --name age  \
    -p 5455:5432 \
    -e POSTGRES_USER=postgresUser \
    -e POSTGRES_PASSWORD=postgresPW \
    -e POSTGRES_DB=postgresDB \
    -d \
    apache/age
```



<h2><img height="20" src="/img/contents.svg">&nbsp;&nbsp;Post Installation</h2>

For every connection of AGE, you start, you will need to load the AGE extension.

```bash
CREATE EXTENSION age;
```
```bash
LOAD 'age';
```
```bash
SET search_path = ag_catalog, "$user", public;
```


<h2><img height="20" src="/img/contents.svg">&nbsp;&nbsp;Quick Start</h2>

To create a graph, use the create_graph function located in the ag_catalog namespace.

```bash
create_graph(graph_name);
```

To create a single vertex, use the CREATE clause. 

```bash
SELECT * 
FROM cypher('graph_name', $$
    CREATE (n)
$$) as (v agtype);
```


To create a single vertex with the label, use the CREATE clause. 

```bash
SELECT * 
FROM cypher('graph_name', $$
    CREATE (:label)
$$) as (v agtype);
```

To query the graph, you can use the MATCH clause.  

```bash
SELECT * FROM cypher('graph_name', $$
MATCH (v)
RETURN v
$$) as (v agtype);
```

You can use the following to create an edge, for example, between two nodes. 

```bash
SELECT * 
FROM cypher('graph_name', $$
    MATCH (a:lable), (b:lable)
    WHERE a.property = 'Node A' AND b.property = 'Node B'
    CREATE (a)-[e:RELTYPE]->(b)
    RETURN e
$$) as (e agtype);
```


To create an edge and set properties.

```bash
SELECT * 
FROM cypher('graph_name', $$
    MATCH (a:label), (b:label)
    WHERE a.property = 'Node A' AND b.property = 'Node B'
    CREATE (a)-[e:RELTYPE {property:a.property + '<->' + b.property}]->(b)
    RETURN e
$$) as (e agtype);
```

Example 

```bash
SELECT * 
FROM cypher('graph_name', $$
    MATCH (a:Person), (b:Person)
    WHERE a.name = 'Node A' AND b.name = 'Node B'
    CREATE (a)-[e:RELTYPE {name:a.name + '<->' + b.name}]->(b)
    RETURN e
$$) as (e agtype);
```



<h2><img height="20" src="/img/gettingstarted.svg">&nbsp;&nbsp;Language Specific Drivers</h2>

Starting with Apache AGE is very simple. You can easily select your platform and incorporate the relevant SDK into your code.

<h4>Built-in</h4>

- [Go driver](./drivers/golang)
- [Java driver](./drivers/jdbc)
- [NodeJs driver](./drivers/nodejs)
- [Python driver](./drivers/python)

<h4>Community-driven Driver</h4>

- [Apache AGE Rust Driver](https://github.com/Dzordzu/rust-apache-age.git)



<h2><img height="20" src="/img/community.svg">&nbsp;&nbsp;Community</h2>

Join the AGE community for help, questions, discussions, and contributions. 

- Check our [website](https://age.apache.org/)
- Chat live with us on [Discord](https://discord.com/invite/NMsBs9X8Ss/)
- Follow us on [Twitter](https://twitter.com/apache_age?s=20&t=7Hu8Txk4vjvuEp-ryakacg)
- Join our [Dev community](https://lists.apache.org/list.html?dev@age.apache.org)


<h2><img height="20" src="/img/visualization.svg">&nbsp;&nbsp;Graph Visualization Tool for AGE</h2>

Apache AGE Viewer is a user interface for Apache AGE that provides visualization and exploration of data.
This web visualization tool allows users to enter complex graph queries and explore the results in graph and table forms.
Apache AGE Viewer is enhanced to proceed with extensive graph data and discover insights through various graph algorithms.
Apache AGE Viewer will become a graph data administration and development platform for Apache AGE to support multiple relational databases: <https://github.com/apache/age-viewer>.

**This is a visualization tool.**
After installing AGE Extension, you may use this tool to get access to the visualization features.

<h2><img height="20" src="/img/contributing.svg">&nbsp;&nbsp;Contributing</h2>

You can improve ongoing efforts or initiate new ones by sending pull requests to [this repository](https://github.com/apache/age).
Also, you can learn from the code review process, how to merge pull requests, and from code style compliance to documentation by visiting the [Apache AGE official site - Developer Guidelines](https://age.apache.org/contribution/guide).
Send all your comments and inquiries to the user mailing list, users@age.apache.org.
