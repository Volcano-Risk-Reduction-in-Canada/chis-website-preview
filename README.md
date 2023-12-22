## Acknowledgement of Docker PHP nginx setup

https://blog.devsense.com/2019/php-nginx-docker

with caveat: extra space needed to be removed from PHP section of docker-compose.yml:

```yaml
volumes:
  - ./data/:/var/www/html/
    - ./logs/php.log:/var/log/fpm-php.www.log
```

```yaml
volumes:
  - ./data/:/var/www/html/
  - ./logs/php.log:/var/log/fpm-php.www.log
```

## Troubleshooting (TODO)

Podman gives this error:

    failed to write to /proc/self/oom_score_adj: Permission denied

See:

- https://github.com/containers/podman/issues/3024
