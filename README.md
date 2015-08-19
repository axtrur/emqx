
## Overview [![Build Status](https://travis-ci.org/emqtt/emqttd.svg?branch=master)](https://travis-ci.org/emqtt/emqttd)

emqttd is a massively scalable and clusterable MQTT V3.1/V3.1.1 broker written in Erlang/OTP. emqttd support both MQTT V3.1/V3.1.1 protocol specification with extended features.

emqttd requires Erlang R17+ to build.


## Goals

emqttd is aimed to provide a solid, enterprise grade, extensible open-source MQTT broker for IoT, M2M and Mobile applications that need to support ten millions of concurrent MQTT clients.

* Easy to install
* Massively scalable
* Easy to extend
* Solid stable


## Features

* Full MQTT V3.1/V3.1.1 protocol specification support
* QoS0, QoS1, QoS2 Publish and Subscribe
* Session Management and Offline Messages
* Retained Messages Support
* Last Will Message Support
* TCP/SSL Connection Support
* MQTT Over Websocket(SSL) Support
* HTTP Publish API Support
* [$SYS/brokers/#](https://github.com/emqtt/emqtt/wiki/$SYS-Topics-of-Broker) Support
* Client Authentication with clientId, ipaddress
* Client Authentication with username, password.
* Client ACL control with ipaddress, clientid, username.
* Cluster brokers on several servers.
* [Bridge](https://github.com/emqtt/emqttd/wiki/Bridge) brokers locally or remotelly
* 500K+ concurrent clients connections per server
* Extensible architecture with Hooks, Modules and Plugins
* Passed eclipse paho interoperability tests


## Modules

* [emqttd_auth_clientid](https://github.com/emqtt/emqttd/wiki/Authentication) - Authentication with ClientIds
* [emqttd_auth_username](https://github.com/emqtt/emqttd/wiki/Authentication) - Authentication with Username and Password
* [emqttd_auth_ldap](https://github.com/emqtt/emqttd/wiki/Authentication) - Authentication with LDAP
* [emqttd_mod_presence](https://github.com/emqtt/emqttd/wiki/Presence) - Publish presence message to $SYS topics when client connected or disconnected
* emqttd_mod_autosub - Subscribe topics when client connected
* [emqttd_mod_rewrite](https://github.com/emqtt/emqttd/wiki/Rewrite) - Topics rewrite like HTTP rewrite module


## Plugins

* [emqttd_plugin_template](https://github.com/emqtt/emqttd_plugin_template) - Plugin template and demo
* [emqttd_dashboard](https://github.com/emqtt/emqttd_dashboard) - Web Dashboard
* [emqttd_plugin_mysql](https://github.com/emqtt/emqttd_plugin_mysql) - Authentication with MySQL
* [emqttd_plugin_pgsql](https://github.com/emqtt/emqttd_plugin_pgsql) - Authentication with PostgreSQL
* [emqttd_plugin_kafka](https://github.com/emqtt/emqttd_plugin_kafka) - Publish MQTT Messages to Kafka
* [emqttd_plugin_redis](https://github.com/emqtt/emqttd_plugin_redis) - Redis Plugin


## Dashboard

The broker released a simple web dashboard in 0.10.0 version.

Address: http://host:18083


## Design

![emqttd architecture](http://emqtt.io/static/img/Architecture.png)


## QuickStart

Download binary packeges for linux, mac and freebsd from [http://emqtt.io/downloads](http://emqtt.io/downloads).

For example:

```sh
unzip emqttd-ubuntu64-0.10.0-beta-20150820.zip && cd emqttd

# start console
./bin/emqttd console

# start as daemon
./bin/emqttd start

# check status
./bin/emqttd_ctl status

# stop
./bin/emqttd stop
``` 

Build from source:

```
git clone https://github.com/emqtt/emqttd.git

cd emqttd && make && make dist
```


## GetStarted

Read [emqtt wiki](https://github.com/emqtt/emqttd/wiki) for detailed installation and configuration guide.


## Benchmark

Benchmark 0.6.1-alpha on a ubuntu/14.04 server with 8 cores, 32G memory from QingCloud:

200K+ Connections, 200K+ Topics, 20K+ In/Out Messages/sec, 20Mbps+ In/Out with 8G Memory, 50%CPU/core


## License

The MIT License (MIT)


## Contributors

* [@callbay](https://github.com/callbay)
* [@hejin1026](https://github.com/hejin1026)
* [@desoulter](https://github.com/desoulter)
* [@turtleDeng](https://github.com/turtleDeng)
* [@Hades32](https://github.com/Hades32)
* [@huangdan](https://github.com/huangdan)
* [@phanimahesh](https://github.com/phanimahesh)
* [@dvliman](https://github.com/dvliman)


## Author

Feng Lee <feng@emqtt.io>


