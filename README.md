Role Name
=========

Install prometheus node exporter in docker using ansible

Requirements
------------

- python-docker or python3-docker pip package
- Docker installed on teh destination host.

Role Variables
--------------

```yaml
# node exporter image version
node_exporter_image_version: v0.18.1
# node exporter Image name
node_exporter_image: "prom/node-exporter"
# node exporter container name:
node_exporter_container_name: node-exporter
# Dicrectory where the test collectors should save files
node_exporter_text_collector_dir: /var/lib/node_exporter/textfile_collector/


# operational flags
# Needed when we want to forcefully restart the container
node_exporter_container_recreate: false
```

Example Playbook
----------------
```yaml
- hosts: all
 - name: Node Exporter
    import_role:
      name: fcastello.node_exporter_docker
```

Limitations
-----------
- Tested only in ubuntu 18.04 and 20.04


License
-------

MIT


