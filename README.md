Repo to recreate telegraf not sending metrics when using `graphite_tag_support = true` from the `postgresql_extensible` plugin

* `$ docker-compose up`
* go to localhost:3000/explore
* enter the following graphite query: `telegraf.postgres.psql.postgres.connections.by.user.count`
* See a graph

Change `graphite_tag_support` to `true` in `telegraf.conf`

* `$ docker-compose down -t 0 && docker-compose up`
* go to localhost:3000/explore
* in the select metric dropdown choose `host` = `telegraf`
* try to find `name = connections.by.user`
* no graph to be seen :(
