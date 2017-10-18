Docker wrapper for wget2. So you don't have to mess up with your host system.

## Run

```
docker run -it --rm hupili/wget2 [options...]
```

For example, downloading in multiple threads:

```
docker run -it --rm hupili/wget2 --chunk-size=10M --max-threads=5 $YOUR_URL
```

Get help:

```
docker run -it --rm hupili/wget2 -h
```

## Build

```
git submodule update --init --recursive
docker-compose build
```
