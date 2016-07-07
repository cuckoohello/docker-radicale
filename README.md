docker-radicale
===============

The [radicale](http//radicale.org/) CalDAV/CardDAV server with default configuration and LDAP support, running in a container.

This is fork of jcsaaddupuy/radicale

Build
------

```
docker build -t radicale .
```

Run it
------

```
docker run -p 5232:5232  radicale
```

or, if you don't want to build it, you can use the pre-built image present on the [registry](https://registry.hub.docker.com/u/gdeflaux/radicale/).

```
docker run -p 5232:5232 gdeflaux/radicale
```


Make data persistents
---------------------

Simply mount a volume to the /data/radicale folder :

```
docker run -p 5232:5232 -v /tmp/radicale/:/data/radicale -i gdeflaux/radicale
```
