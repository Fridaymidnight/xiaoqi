---
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: false
      related: true
title:  "[Solved] git merge conflict"
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
