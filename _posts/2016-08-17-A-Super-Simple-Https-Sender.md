---
layout: post
title: A Super Simple Https Sender
---
A java http SSL/TLS connection sender that breaks all the security rules.

Because who needs security anyway?! Only terrorists and wimps! Ok maybe not, but in order to understand how the security actually works there is no better way than to try to break it first.

The clue is in these few lines that override the default java hostname and certificate verifiers.
We replace them here with our own versions that trust all input by doing absolutely nothing.
See their implementation further along in the code.
[github](https://github.com/CarpeScientia/SuperSimpleHttpsSender.git)

``` java
			SSLContext sc = SSLContext.getInstance("TLS");
			sc.init(null, trustAllCerts, new java.security.SecureRandom());
			HttpsURLConnection.setDefaultSSLSocketFactory(sc.getSocketFactory());
			HttpsURLConnection.setDefaultHostnameVerifier(trustAllHosts);
```

Now obviously putting code like this live is a very bad idea, but if you want to restrict the https connections that are allowed to go out to a very specific few this is where you start. 
