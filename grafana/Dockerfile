FROM grafana/grafana:12.0.1

WORKDIR /worker
USER root
RUN wget -O aliyun-log-grafana-datasource-plugin-master.zip https://github.com/aliyun/aliyun-log-grafana-datasource-plugin/archive/refs/heads/master.zip \
    && unzip aliyun-log-grafana-datasource-plugin-master.zip -d /var/lib/grafana/plugins \
    && sed -i '/;allow_loading_unsigned_plugins =/a\allow_loading_unsigned_plugins = aliyun-log-service-datasource' /etc/grafana/grafana.ini

WORKDIR /usr/share/grafana
USER grafana