FROM library/logstash:1.5.0

# TODO 规范化配置文件处理
COPY ./configs.conf /
ENV LOGSTASH_CONFIG /configs.conf

# 默认程序入口
COPY ./docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
