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

[To generate self-signed ssl certificate in a single command line without user interaction](http://docs.oracle.com/javase/6/docs/technotes/tools/solaris/keytool.html#EXAMPLES):

```
keytool -genkey -alias tomcat -keyalg RSA -storepass changeit -keypass changeit -dname "cn=Frank R., ou=Study Jams, o=GDG Suzhou, l=Suzhou, st=Jiangsu, c=CN"
```

To list:

```
keytool -list -alias tomcat -storepass changeit
```

To removed the certifcate:

```
keytool -delete -alias tomcat -storepass changeit
```

Note: Tomcat doesn't support soft link inside a exploded war (nor does Chrome Dev Editor)

# TODO How to setup ports, HTTP (80) and HTTPS (443)
