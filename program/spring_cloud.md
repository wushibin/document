# Spring Cloud

## Spring cloud configure

### Enable/Disable a component (starter) during the unit test 

Create a bootstrap.yml file under the test.resource folder.
For example if you want to disable some function of zookeeper:

- If you want to disable the all the zookeeper, make the zookeepter.enable to false.
- If you want to disable the zookeeper config, make the zookeeper.config.enable to false.

```
spring:
  cloud:
    zookeeper:
      enabled: true
      config:
        enabled: false
        root: configuration
        defaultContext: apps
        profileSeparator: '::'
```