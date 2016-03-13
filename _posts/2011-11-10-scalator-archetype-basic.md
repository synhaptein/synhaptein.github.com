---
layout: post
title: Scalator-archetype-basic update
categories: [scalator]
tags: []
description:
---

Here is an updated snapshot of the basic archetype that works with the latest scalator development.

<p>Create a new project:</p>
<div class="codeblock">
{% highlight bash %}
mvn archetype:generate -U \
   -DarchetypeGroupId=com.synhaptein \
   -DarchetypeArtifactId=scalator-archetype-basic \
   -DarchetypeVersion=0.3-SNAPSHOT \
   -DgroupId=com.example.yourapp -DartifactId=yourapp
{% endhighlight %}
</div>

<p>Run the helloworld:</p>
<div class="codeblock">
{% highlight bash %}
maven jetty:run
{% endhighlight %}
</div>

<p>Now you should be able to connect to <a class="readmore" href="http://localhost:8080/testweb/">http://localhost:8080/testweb/</a></p>
<p><span class="important">Edited on Feb. 14, 2012</span>: scalator is now hosted on oss sonatype</p>