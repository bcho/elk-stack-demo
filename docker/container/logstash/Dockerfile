FROM library/logstash:1.5.0

# TODO 规范化配置文件处理
COPY ./configs.conf /
ENV LOGSTASH_CONFIG /configs.conf

COPY ./ssl.cert /ssl.cert
ENV LOGSTASH_SSL_CERT /ssl.cert
COPY ./ssl.key /ssl.key
ENV LOGSTASH_SSL_KEY /ssl.key

COPY ./grok-patterns /grok-patterns
ENV GROK_PATTERNS /grok-patterns


# 默认程序入口
COPY ./docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
