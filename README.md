# ansible-role-kafka

## Purpose
This ansible role installs kafka cluster or standalone instance based on KRaft protocol.

## Configuration

| Variable | Description | Default |
| ------ | ------ | ------ |
| kafka_version | Kafka version | 3.4.0 |
| kafka_scala_version | Kafka scala version | 2.13 |
| kafka_openjdk_version | Kafka OpenJDK version | 17 |
| kafka_download_url | Kafka archive download url | `https://dlcdn.apache.org/kafka/{{ kafka_version }}/kafka_{{ kafka_scala_version }}-{{ kafka_version }}.tgz` |
| kafka_hosts_group | Kafka hosts group in ansible inventory | kafka |
| kafka_user | Kafka user | kafka |
| kafka_group | Kafka group | kafka |
| kafka_config_directory | Kafka config directory | `/etc/kafka` |
| kafka_data_directory | Kafka data directory | `/var/lib/kafka` |
| kafka_log_directory | Kafka log directory | `/var/log/kafka` |
| kafka_extra_files | Defines extra files with some content. Files are located in `kafka_config_directory` | {} |
| kafka_extra_envs | Defines extra environment variables | {} |
| kafka_server_properties | Defines extra parameters in server.properties config | {} |
| kafka_log4j_properties | Overrides default log4j.properties | "" |
| kafka_sasl_enabled | Enables/Disables SASL | false |
| kafka_password | Password of kafka user (If SASL is enabled) | "changeMe" |
| kafka_users | Defines other users if it is required (if SASL is enablede) | `{admin.password: "changeMe"}` |
| kafka_opts | Defines KAFKA_OPTS environment variable | "" |
