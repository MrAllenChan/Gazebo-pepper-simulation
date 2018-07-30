# Notes about configuring gzweb
* Author: Allen Chan
* Created: 2018-07-28
* Updated: 2018-07-30

Related websites and tutorials:
* [Gzweb installation](http://gazebosim.org/tutorials?tut=gzweb_install&cat=gzweb#Running)
* [Gzweb: Web client for Gazebo](http://gazebosim.org/gzweb#install-collapse-2)
* [Websocket and HTTP](https://www.cnblogs.com/fuqiang88/p/5956363.html)
* [WebSocket 教程](http://www.ruanyifeng.com/blog/2017/05/websocket.html)

## Running GzWeb involves the following pieces:

* gzserver running the headless Gazebo simulation (runs by default on http://127.0.0.1:11345)

* GzWeb's NodeJS server which communicates with gzserver using Gazebo Transport. It works as a bridge between the Javascript and the C++ code.

* An HTTP server which serves static content such as models and website assets (icons, HTML, CSS, client-side Javascript...)

* A Websocket server which forwards simulation updates coming from gzserver to the browser

* A browser client which connects to the HTTP and websocket servers
