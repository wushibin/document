# Java 调优

## 教程启动jstated

参考: https://yq.aliyun.com/articles/38757

- 新建jstatd.all.policy文件

```shell
vi jstatd.all.policy

grant codebase "file:${java.home}/../lib/tools.jar" { 
   permission java.security.AllPermission; 
};
```

- 启动jstated服务

```shell
jstatd -J-Djava.security.policy=jstatd.all.policy -J-Djava.rmi.server.hostname=172.16.30.12
```


## HeapDump

```shell
# 历史内存快照（从JVM启动到当前时刻）
jmap -dump:format=b,file=/data/heap.hprof pid   
# 当前内存快照
jmap -dump:live,format=b,file=/data/heap_live.hprof pid  
```


http://www.rowkey.me/blog/2016/11/02/java-profile/