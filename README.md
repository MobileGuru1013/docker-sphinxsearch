# docker-sphinxsearch
Docker image for [Sphinx search engine](http://sphinxsearch.com/docs/sphinx3.html)

```
docker pull macbre/sphinxsearch
```

## Usage example

You can use this image in `docker-compose`-powered app:

```yaml
services:
  sphinx:
    image: macbre/sphinxsearch:3.0.1
    ports:
    - "127.0.0.1:36307:36307" # bind to local interface only!
    volumes:
    - ./data:/opt/sphinx/index  # directory where sphinx will store index data
    - ./sphinx.conf:/opt/sphinx/conf/sphinx.conf  # SphinxSE configuration file
    mem_limit: 512m # match indexer.value from sphinx.conf
```

## [Tags available](https://hub.docker.com/r/macbre/sphinxsearch/tags/)

### `3.1.1`, `latest`

Built on: Linux alpine38 4.14.69-0-vanilla #1-Alpine SMP Mon Sep 10 19:33:23 UTC 2018 x86_64 Linux
Built with: gcc 6.4.0
Build date: Oct 17 2018
Build type: release
Configure flags:  '--enable-dl' '--with-mysql' '--with-pgsql' '--with-unixodbc' 'CXXFLAGS=-DSPHINX_TAG= -DNDEBUG -O3 -g1 -D__MUSL__' 'LDFLAGS=-static-libstdc++ -static-libgcc'
Compiled DB drivers: mysql-dynamic pgsql-dynamic odbc-dynamic
Enabled dynamic drivers: mysql pgsql
```

### `3.0.3`

Built on: Linux ubuntu16 4.4.0-116-generic #140-Ubuntu SMP Mon Feb 12 21:23:04 UTC 2018 x86_64 x86_64 x86_64 GNU/Linux
Built with: gcc 5.4.0
Build date: Mar 30 2018
Build type: release
Configure flags:  '--enable-dl' '--with-mysql' '--with-pgsql' '--with-unixodbc' 'CXXFLAGS=-DSPHINX_TAG= -DNDEBUG -O3 -g1' 'LDFLAGS=-static-libstdc++'
Compiled DB drivers: mysql-dynamic pgsql-dynamic odbc-dynamic
Enabled dynamic drivers: mysql pgsql
```

### `3.0.1`

Built on: Linux ubuntu16desktop 4.4.0-101-generic #124-Ubuntu SMP Fri Nov 10 18:29:59 UTC 2017 x86_64 x86_64 x86_64 GNU/Linux
Built with: gcc 5.4.0
Build date: Dec 17 2017
Build type: release
Configure flags:  '--enable-dl' '--with-mysql' '--with-pgsql' 'CXXFLAGS=-DSPHINX_TAG= -g1' 'LDFLAGS=-static-libstdc++'
Compiled DB drivers: mysql-dynamic pgsql-dynamic
Enabled dynamic drivers: mysql pgsql
```
