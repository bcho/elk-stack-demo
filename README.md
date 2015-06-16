# ELK Stack

## 生成 tls/ssl 认证文件

```bash
$ openssl req -x509  -batch -nodes -newkey rsa:2048 -keyout lumberjack.key -out lumberjack.crt -subj /CN=logstash-remote
```

生成后请分别复制一份到 `docker/container/logstash` 和 `logstash-forwarder/` 下。

[reference](https://github.com/elastic/logstash-forwarder#important-tlsssl-certificate-notes)


## 运行

### 构建 docker images

```bash
$ cd docker
$ docker-compose build
$ docker-compose up
```

### 运行 kibana

http://docker-ip:5601


### 运行 logstash-forwarder

```bash
$ cd logstash-forwarder
$ ./logstash-forwarder -config config.json
```


## LICENSE

CC 4.0
