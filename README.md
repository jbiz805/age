<br>

<p align="center">
     <img src="https://age.apache.org/age-manual/master/_static/logo.png" width="30%" height="30%">
</p>
<br>

<h3 align="center">
    <a href="https://surrealdb.com#gh-dark-mode-only" target="_blank">
        <img src="https://age.apache.org/age-manual/master/_static/logo.png" height="30" alt="AGE DB">
    </a>
   
    is the multimodel <br> database for tomorrow's applications
</h3>




<br>

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

[Apache AGE](https://age.apache.org/#) is a PostgreSQL Extension that provides graph database functionality. AGE is an acronym for A Graph Extension, and is inspired by Bitnine's AgensGraph, a multimodel database fork of PostgreSQL. The goal of the project is to enable users of Postgres to use graph query modeling in unison with Postgres' existing relational model.

A graph consists of a set of vertices (also called nodes) and edges, where each individual vertex and edge possesses a map of properties. A vertex is the basic object of a graph, that can exist independently of everything else in the graph. An edge creates a directed connection between two vertices. A graph database is simply composed of vertices and edges. This type of database is useful when the meaning is in the relationships between the data. Relational databases can easily handle direct relationships, but indirect relationships are more difficult to deal with in relational databases. A graph database stores relationship information as a first-class entity. Apache AGE gives you the best of both worlds, simultaneously.

Apache AGE is:

- **Powerful**: adds graph database support to the already popular PostgreSQL database: PostgreSQL is used by organizations including Apple, Spotify, and NASA.
- **Flexible**: allows you to perform openCypher queries, which make complex queries much easier to write.
- **Intelligent**: allows you to perform graph queries that are the basis for many next level web services such as fraud detection, master data management, product recommendations, identity and relationship management, experience personalization, knowledge management and more.

Also, while the technology can be integrated against many data layers, a graph database is also the perfect companion for a [GraphQL](https://graphql.org/) API. Since the information is already in a native format, it simplifies many factors and even allows many operations to be generated automatically. GraphQL is rapidly  superceeding REST as the standard for cloud applications. 

## Overview

- **Apache AGE is currently being developed for the PostgreSQL 12 release** and will support PostgreSQL 13 and all the future releases of PostgreSQL.
- Apache AGE supports the openCypher graph query language.
- Apache AGE enables querying multiple graphs at the same time.
- The goal of Apache AGE is to make it compatible with all relational databases in the future.

## Latest Events

- Latest Apache AGE release, [Apache AGE 1.1.0](https://github.com/apache/age/releases/tag/v1.1.0-rc0).
- Renewed Apache AGE homepage - [Apache AGE website](http://age.apache.org/).
- Send all your comments and inquiries to the user mailing list, users@age.apache.org.
- Support for PostgreSQL will be added in the Q4 2022 to focus more on implementing the openCypher specification.

## Documentation

Refer to our latest [Apache AGE documentation](https://age.apache.org/age-manual/master/index.html) to learn about installation, features and built-in functions, and  Cypher queries.

## Installation

- [Installing from source](https://age.apache.org/download)
- [Apache AGE setup guide](https://age.apache.org/age-manual/master/intro/setup.html#)
- [Installing via docker image](https://age.apache.org/age-manual/master/intro/setup.html#installing-via-docker-image)

## Language Specific Drivers

### Built-in

- [Go driver](./drivers/golang)
- [Java driver](./drivers/jdbc)
- [NodeJs driver](./drivers/nodejs)
- [Python driver](./drivers/python)

### Community-driven Driver
- [Apache AGE Rust Driver](https://github.com/Dzordzu/rust-apache-age.git)

## Graph Visualization Tool for AGE

Apache AGE Viewer is a user interface for Apache AGE that provides visualization and exploration of data.
Through this simple web visualization tool, users can enter complex graph queries and explore the results in graph and table forms.
Apache AGE Viewer is enhanced to proceed with large graph data and discover the insights through various graph algorithms.
Apache AGE Viewer will become a graph data administration and development platform for Apache AGE to support multiple relational databases: <https://github.com/apache/age-viewer>.

- This is a visualization tool.
After installing AGE Extension, you may use this tool to get access to the visualization features.

## Contribution

You can improve ongoing efforts or initiate new ones by sending pull requests to [this repository](https://github.com/apache/age).
Also, you can learn from the code review process, how to merge pull requests, and from code style compliance to documentation, by visiting the [Apache AGE official site - Developer Guidelines](https://age.apache.org/contribution/guide).
