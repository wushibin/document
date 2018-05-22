# Mvn Usage

### Display the depence tree

    mvn dependency:tree

### Generate project

```shell
 mvn archetype:generate -DgroupId=spring.cloud.on.docker -DartifactId=config-server -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

### Compiler Error

#### use -source 7 or higher

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-compiler-plugin</artifactId>
    <version>3.1</version>
    <configuration>
        <source>1.7</source>
        <target>1.7</target>
    </configuration>
</plugin>
```

Or 

```
<maven.compiler.source>1.8</maven.compiler.source>
<maven.compiler.target>1.8</maven.compiler.target>
```

Refer to: https://stackoverflow.com/questions/29258141/maven-compilation-error-use-source-7-or-higher-to-enable-diamond-operator