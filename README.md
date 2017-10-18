Docker wrapper for wget2. So you don't have to mess up with your host system.

## Run

```
docker run --rm hupili/wget2 [options...]
```

For example, downloading in multiple threads and put the downloaded content in current working directory: (the working dirctory in container is `/data`)

```
docker run -v $PWD:/data --rm hupili/wget2 --chunk-size=1M --max-threads=4 $YOUR_URL
```

(Docker seems to have problems when thread number is greater than the core number of docker machine)

Get help:

```
docker run --rm hupili/wget2 -h
```

## Build

Build only if you want. Docker will automatically pull images, so the above command works just off-the-shelf.

```
git submodule update --init --recursive
docker-compose build
```

## Release

This note is only for myself:

```
docker push hupili/wget2
```
