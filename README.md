# ansible-role-kafka

## Purpose
This ansible role installs kafka cluster or standalone instance based on KRaft protocol.

## Example of inventory and playbook
1) inventory file
```ini
[kafka]
kafka-1.example.com kafka_node_id=1 kafka_process_roles=broker,controller
kafka-2.example.com kafka_node_id=2 kafka_process_roles=broker,controller
kafka-3.example.com kafka_node_id=3 kafka_process_roles=broker,controller
```
2) Playbook
```yaml
---
- hosts: kafka
  become: true
  gather_facts: false
  roles:
    - role: m_shalenko.ansible_role_kafka
      tags:
        - kafka
```
