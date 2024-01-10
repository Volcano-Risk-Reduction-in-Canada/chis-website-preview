# CHIS Website Preview

This git repository contains an NGINX + PHP Docker Compose application
which allows easy editing and live-previewing a local copy of
the CHIS website.

It also uses a GitHub Actions workflow to generate a staging preview
of proposed changes to the CHIS website, hosted on GitHub Pages,
to facilitate collaboration and review.  It is publicly accessible
at <https://volcano-risk-reduction-in-canada.github.io/chis-website-preview/>.

Examples:

- Addition of the new [Volcano Risk Reduction in Canada (VRRC) landing page](https://volcano-risk-reduction-in-canada.github.io/chis-website-preview/volcano-volcan/risk-reduction-des-risques-en.html) ([français](https://volcano-risk-reduction-in-canada.github.io/chis-website-preview/volcano-volcan/risk-reduction-des-risques-fr.html))

- Update of the [Debris Flow Impact Database page](https://volcano-risk-reduction-in-canada.github.io/chis-website-preview/DFID-BDICD/index-en.html) ([français](https://volcano-risk-reduction-in-canada.github.io/chis-website-preview/DFID-BDICD/index-fr.html)

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
