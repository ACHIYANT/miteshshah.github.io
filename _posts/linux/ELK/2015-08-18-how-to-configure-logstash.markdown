---
layout: post
title: How to Configure Logstash
author:
modified:
comments: true
categories: linux/ELK
excerpt: "Step by step guide to configure Logstash - Transport and process your logs, events, or other data"
tags: [Linux, ELK, Logstash, Devops]
image:
  url:
  alt:
  title:
  feature:
date: 2015-08-18T14:27:53+05:30
---

{% include _toc.html %}

### Configure Logstash

* For Logstash, We have to create/update configuration file.

{% highlight bash %}
$ cat /etc/logstash/conf.d/logstash.conf
output {
  elasticsearch {
    # Don't required for local ElasticSearch
    # cluster  => Gateway # This matches out elasticsearch cluster.name
    # protocol => http
  }
}
{% endhighlight %}


### Restart Logstash Service

{% highlight bash %}
$ sudo service logstash restart
{% endhighlight %}
