---
layout: post
title:  "solving git merge conflict"
date:   2018-10-31 12:59:49 -0700
---


{% highlight ruby %}
 (master|MERGING)
$ git pull
error: You have not concluded your merge (MERGE_HEAD exists).
hint: Please, commit your changes before merging.
fatal: Exiting because of unfinished merge.
{% endhighlight %}

Try

{% highlight ruby %}
$ git merge --abort
{% endhighlight %}
