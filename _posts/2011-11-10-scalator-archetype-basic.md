---
layout: post
title: Scalator-archetype-basic update
categories: [scalator]
tags: []
description:
---

Here is an updated snapshot of the basic archetype that works with the latest scalator development.

Create a new project:

``` bash
mvn archetype:generate -U \
   -DarchetypeGroupId=com.synhaptein \
   -DarchetypeArtifactId=scalator-archetype-basic \
   -DarchetypeVersion=0.3-SNAPSHOT \
   -DgroupId=com.example.yourapp -DartifactId=yourapp
```

Run the helloworld:
``` bash
maven jetty:run
```

Now you should be able to connect to [http://localhost:8080/testweb/](http://localhost:8080/testweb/)

<span class="important">Edited on Feb. 14, 2012</span>: scalator is now hosted on oss sonatype
