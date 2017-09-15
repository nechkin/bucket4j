# Bucket4j - is a java implementation of token-bucket algorithm for rate limiting
[![Build Status](https://travis-ci.org/vladimir-bukhtoyarov/bucket4j.svg?branch=master)](https://travis-ci.org/vladimir-bukhtoyarov/bucket4j)
[![Join the chat at https://gitter.im/vladimir-bukhtoyarov/bucket4j](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/vladimir-bukhtoyarov/bucket4j?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Quality Gate](https://sonarqube.com/api/badges/gate?key=com.github.vladimir-bukhtoyarov:bucket4j)](https://sonarqube.com/dashboard/index/com.github.vladimir-bukhtoyarov:bucket4j)

## Advantages of Bucket4j
* Implemented on top of ideas of well known algorithm, which are by de-facto standard for rate limiting in the IT industry.
* Effective lock-free implementation, Bucket4j is good scalable for multithreading case.
* Absolutely non-compromise precision, Bucket4j does not operate with floats or doubles, all calculation are performed in the integer arithmetic,
this feature protects end users from calculation errors involved by rounding.
* Ability to switch from one JVM to cluster in two lines of code. Using Bucket4j you are able to limiting something in the cluster of JVMs.
Since [release 1.2](https://github.com/vladimir-bukhtoyarov/bucket4j/releases/tag/1.2.0) the ```Bucket4j``` supports any GRID solution which compatible with [JCache API (JSR 107)](https://www.jcp.org/en/jsr/detail?id=107) specification.
Just use your favorite grid including [Hazelcast](http://hazelcast.com/products/hazelcast/), [Ignite](https://ignite.apache.org/), [Coherence](http://www.oracle.com/technetwork/middleware/coherence/overview/index.html), [Infinispan](http://infinispan.org/) or any other.
* Ability to specify multiple bandwidths per bucket. For example you can limit 1000 events per hours but not often then 100 events per minute.
* Both synchronous and asynchronous API.

## Documentation
* [Basic-usage](doc-pages/basic-usage.md) - examples of basic usage, just start from here and most likely you will skip the rest items below. 
* [Brief overview of token-bucket algorithm](doc-pages/token-bucket-brief-overview.md) - the brief overview of token-bucket algorithm.
* [Bucket4j key concepts](doc-pages/key-concepts.md) describes main terms, technical limits and algorithms used inside Bucket4j.
* [Advanced usage](doc-pages/advanced-usage.md) - examples of advanced usage. 
* [Documentation for previous versions](doc-pages/archive-links.md)

## Supported back-ends
* [Jcache integration](doc-pages/jcache-usage.md) - documentation and examples about usage ```Bucket4j``` with in-memory grids which supports ```JCache API (JSR 107)``` specification. 
* [Hazelcast integration](doc-pages/hazelcast.md) - documentation and examples for ```bucket4j-hazelcast``` module.
* [Apache Ignite integration](doc-pages/ignite.md) - documentation and examples for ```bucket4j-ignite``` module.
* [Infinspan integration](doc-pages/inifinispan.md) - documentation and examples for ```bucket4j-infinispan``` module.
* [Spring Boot Starter](https://github.com/MarcGiffing/bucket4j-spring-boot-starter) - third-party integration developed by @MarcGiffing.

## Third-party integrations:
* [Spring Boot Starter for Bucket4j](https://github.com/MarcGiffing/bucket4j-spring-boot-starter) 
* [JHipster API Gateway](https://jhipster.github.io/api-gateway/#rate_limiting)
* [Dropwizard Ratelimit](https://github.com/zivver/dropwizard-ratelimit)

## Get Bucket4j library
#### By direct link
[Download compiled jar, sources, javadocs](https://github.com/vladimir-bukhtoyarov/bucket4j/releases/tag/3.0.0)

#### You can build Bucket4j from sources
```bash
git clone https://github.com/vladimir-bukhtoyarov/bucket4j.git
cd bucket4j
mvn clean install
```

#### You can add Bucket4j to your project as maven dependency
The Bucket4j is distributed through both [JCenter](https://bintray.com/bintray/jcenter) and [Maven Central](http://search.maven.org/),
use any of them:
```xml
<dependency>
    <groupId>com.github.vladimir-bukhtoyarov</groupId>
    <artifactId>bucket4j-core</artifactId>
    <version>3.0.0</version>
</dependency>
```

## Have a question?
Feel free to ask in the [gitter chat](https://gitter.im/vladimir-bukhtoyarov/bucket4j) 

## License
Copyright 2015-2017 Vladimir Bukhtoyarov
Licensed under the Apache Software License, Version 2.0: <http://www.apache.org/licenses/LICENSE-2.0>.

