This has been generated by the StormCrawler Maven Archetype as a starting point for building your own crawler.
Have a look at the code and resources and modify them to your heart's content. 

With Storm installed, you must first generate an uberjar:

``` sh
mvn clean package
```

before submitting the topology using the storm command:

``` sh
storm jar target/${artifactId}-${version}.jar ${package}.CrawlTopology -conf crawler-conf.yaml -local
```

This will run the topology in local mode. Simply remove the '-local' to run the topology in distributed mode.

You can also use Flux to do the same:

``` sh
storm jar target/${artifactId}-${version}.jar  org.apache.storm.flux.Flux --local crawler.flux
```
