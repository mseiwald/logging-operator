# Kafka output plugin for Fluentd
## Overview
 More info at https://github.com/uken/fluent-plugin-elasticsearch

## Configuration
### Kafka
#### Send your logs to Kafka

| Variable Name | Type | Required | Default | Description |
|---|---|---|---|---|
| brokers | string | Yes | - | The list of all seed brokers, with their host and port information.<br> |
| topic_key | string | No |  "topic" | Topic Key <br> |
| partition_key | string | No |  "partition" | Partition <br> |
| partition_key_key | string | No |  "partition_key" | Partition Key <br> |
| message_key_key | string | No |  "message_key" | Message Key <br> |
| default_topic | string | No |  nil | The name of default topic .<br> |
| default_partition_key | string | No |  nil | The name of default partition key .<br> |
| default_message_key | string | No |  nil | The name of default message key .<br> |
| exclude_topic_key | bool | No |  false | Exclude Topic key <br> |
| exclude_partion_key | bool | No |  false | Exclude Partition key <br> |
| get_kafka_client_log | bool | No |  false | Get Kafka Client log <br> |
| headers | map[string]string | No |  {} | Headers <br> |
| headers_from_record | map[string]string | No |  {} | Headers from Record <br> |
| use_default_for_unknown_topic | bool | No |  false | Use default for unknown topics <br> |
| idempotent | bool | No |  false | Idempotent <br> |
| sasl_over_ssl | bool | No |  false | SASL over SSL <br> |
| max_send_retries | int | No |  1 | Number of times to retry sending of messages to a leader <br> |
| required_acks | int | No |  -1 | The number of acks required per request .<br> |
| ack_timeout | int | No |  nil => Uses default of ruby-kafka library | How long the producer waits for acks. The unit is seconds <br> |
| compression_codec | string | No |  nil | The codec the producer uses to compress messages . The available options are gzip and snappy.<br> |
| buffer_topic | *Buffer | No | - |  |