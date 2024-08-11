# All-in-one ShardingSphere-JDBC

Pain point:
* The official release of ShardingSphere-JDBC does not provide a single JAR file that contains all dependencies.
* ShardingSphere-JDBC is a collection of multiple modules, and it is not easy to build a single JAR file that contains all dependencies.

## Building all-in-one ShardingSphere-JDBC JAR

Standalone mode (without ZooKeeper or other cluster dependencies):
```shell
./mvnw clean package
```

Cluster mode (with ZooKeeper Curator)
```shell
./mvnw clean package -Pcluster
```

## Add ShardingSphere-JDBC to your project

```shell
ls -hl target/shardingsphere-jdbc-*.jar
```
```
-rw-rw-r-- 1 wuweijie wuweijie 55M Aug 11 16:10 target/shardingsphere-jdbc-standalone-5.5.1-SNAPSHOT.jar
-rw-rw-r-- 1 wuweijie wuweijie 26M Aug 11 16:10 target/shardingsphere-jdbc-standalone-5.5.1-SNAPSHOT-sources.jar
```


TODO:
* [ ] Shade third party dependencies
* [ ] Add more profiles for different use cases
