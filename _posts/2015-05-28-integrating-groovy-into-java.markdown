---
layout: post
title:  "Integrating Groovy into Java"
date:   2015-05-28 14:02:00
categories: java groovy
---

We are creating an Apache Flume interceptor at work. We are attempting to make it as generic as possible and allow us
to customize our needs to it purely by way of the flume configuration.

Currently the interceptor takes data, we provide it with keys/tokens in the configuration of the interceptor in the flume
configuration file and then it converts said data into a json object. We do not want to create custom code for every situation
in the interceptor class, so we opted to use groovy scripts.

What we did is allow the user to create groovy scripts in the configuration file, which then get applied to the json 
transformation occurring in the interceptor. Pretty cool stuff.

I found the groovy docs to be very informative here, specifically section 3.13.3:
http://docs.groovy-lang.org/latest/html/documentation/index.html#_integrating_groovy_in_a_java_application