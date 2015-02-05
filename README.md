# studyjams.dushu.hu

This is the source code for the web site, http://studyjams.dushu.hu

You can also host a clone on your LAN. Here is how.
```
git clone https://github.com/studyjams/studyjams.github.io
cd studyjams.github.io
git clone https://github.com/renfeng/android-repository script
```
this will require at least 11GB not including the storage for studio and sdk manager.
```
script/download.sh
```

You'll need a web server to host the web site. I'm using tomcat on Windows because, I can use a zip version, and it's easy to setup [https](http://tomcat.apache.org/tomcat-6.0-doc/ssl-howto.html#Quick_Start). https is for quick failover when fetching [repository-10.xml and addons_list-2.xml](https://github.com/renfeng/android-repository/issues/1)
