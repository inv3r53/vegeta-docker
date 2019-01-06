# Vegeta Docker
[![](https://images.microbadger.com/badges/image/peterevans/vegeta.svg)](https://microbadger.com/images/peterevans/vegeta)
[![Build Status](https://travis-ci.org/peter-evans/vegeta-docker.svg?branch=master)](https://travis-ci.org/peter-evans/vegeta-docker)

Docker image for the [Vegeta](https://github.com/tsenart/vegeta) HTTP load testing tool.

## Supported tags and respective `Dockerfile` links

- [`6.2.0`, `6.2`, `latest`  (*6.2/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/6.2)
- [`6.1.0`, `6.1`  (*6.1/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/6.1)
- [`6.0.0`, `6.0`  (*6.0/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/6.0)
- [`5.1.0`, `5.1`  (*5.1/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/5.1)
- [`5.0.0`, `5.0`  (*5.0/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/5.0)
- [`4.0.0`, `4.0`  (*4.0/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/4.0)
- [`3.1.1`, `3.1`  (*3.1/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/3.1)
- [`3.0.0`, `3.0`  (*3.0/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/3.0)
- [`2.0.1`, `2.0`  (*2.0/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/2.0)
- [`1.3.0`, `1.3`  (*1.3/Dockerfile*)](https://github.com/peter-evans/vegeta-docker/tree/master/1.3)

For earlier versions see [releases](https://github.com/peter-evans/vegeta-docker/releases) and the available [tags on Docker Hub](https://hub.docker.com/r/peterevans/vegeta/tags/).

## Usage

To display help:
```bash
docker run --rm -i peterevans/vegeta
```
Example:
```bash
docker run --rm -i peterevans/vegeta sh -c \
"echo 'GET https://www.example.com' | vegeta attack -rate=10 -duration=30s | tee results.bin | vegeta report"
```
For full documentation see [Vegeta](https://github.com/tsenart/vegeta).

## Usage in Kubernetes

To display help:
```bash
kubectl run vegeta --rm --attach --restart=Never --image="peterevans/vegeta"
```
Example:
```bash
kubectl run vegeta --rm --attach --restart=Never --image="peterevans/vegeta" -- sh -c \
"echo 'GET https://www.example.com' | vegeta attack -rate=10 -duration=30s | tee results.bin | vegeta report"
```

## License

MIT License - see the [LICENSE](LICENSE) file for details
