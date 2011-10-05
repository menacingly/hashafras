Hashafras
========

A really tiny consistent hashing library for Ruby

Use
---

    ring = Hashafras::Ring.new
    ring.add_member("foo", "10.10.10.9:8080")
    ring.add_member("bar", "10.10.10.10:8080")
    ring["some_key"] # "10.10.10.10:8080"
    ring["some_other_key"] # "10.10.10.9:8080"


Props
------

Big ups to Superfeedr for his [solid implementation](https://github.com/superfeedr/consistent_hashr) I referenced 

And of course Mike Perham for his near-ubiquitous [explanation of consistent hashing](http://www.mikeperham.com/2009/01/14/consistent-hashing-in-memcache-client/).
