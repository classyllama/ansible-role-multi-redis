# Ansible Redis

* For multiple redis instance setups
* Installs redis30u from IUS repo
* Supports RHEL 6 / 7

## Example Usage

* Prod triple-redis setup:

        - { name: redis, redis_instance: { name: obj, port: 6379 }}
        - { name: redis, redis_instance: { name: fpc, port: 6381 }}
        - { name: redis, redis_instance: { name: ses, port: 6380, save: yes }}

* Stage triple-redis setup:

        - { name: redis, redis_instance: { name: stage-obj, port: 6389 }}
        - { name: redis, redis_instance: { name: stage-fpc, port: 6391 }}
        - { name: redis, redis_instance: { name: stage-ses, port: 6390, save: yes }}

