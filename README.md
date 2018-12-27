# amazonriver

amazonriver 是一个将postgresql的实时数据同步到es或kafka的服务

## 原理

amazonriver 利用pg内部的逻辑复制功能,通过在pg创建逻辑复制槽,接收数据库的逻辑变更,通过解析test_decoding特定格式的消息,得到逻辑数据

## 安装使用

### 安装

```shell
$git clone https://github.com/hellobike/amazonriver
$cd amazonriver
$glide install
$go install
```

### 使用

    amazonriver -configs config.json

## PG 配置

PG数据库需要预先开启逻辑复制[pg配置](./doc/pg.md)

## amazonriver 配置

### 监控

amazonriver支持使用prometheus来监控同步数据状态,[配置Grafana监控](./doc/prometheus.md)

### 同步到 elasticsearch

[同步到elasticsearch](./doc/es.md)

### 同步到 kafka

[同步到kafka](./doc/kafka.md)

## 许可

amazonriver 使用 Apache License 2 许可