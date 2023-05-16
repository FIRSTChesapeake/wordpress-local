# Overview

This is a basic docker compose script to startup and run a local wordpress instance for experimentation and local development if needed.  It is not intended for production and is just a utility script.

## Running

The docker compose file should contain everything you need to initiate and run a site. 

The following will initiate a new site if one does not exist.  If a site exists (you'll have data, plugins, and wordpress subdirectories) it will start a site with that data, but it is faster and more efficient to use docker-compose start below.
```
> docker-compose up -d
```

To bring the docker images down and delete them use:\
```
> docker-compose down
```
Note if you want to just stop the site and start working on it again later, use docker-compose stop below, it's faster and more efficient.

## Starting and Stopping.

Any site you create locally with this should persist if you use the start and stop command.  Note that you should not rely on this to retain any serious work as it might fail but if you're just tinkering around this will work.

```
> docker-compose start
```
and
```
> docker-compose stop
```

### Restarting a site from scratch.

If you want to restart a new wordpress instance from scratch and do away with everything you've done so far, just delete the data, plugins, and wordpress directories. They will be automatically recreated when you do another docker-compose up.

## Accessing the site

When the site is running you can access via http://localhost:4000