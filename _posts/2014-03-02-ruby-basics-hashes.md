---
layout: post
title:  "Ruby Hash"
date:   2014-03-02 11:26:42
language: ruby
tags: free ruby coding resources hash
categories: basics
repo: https://github.com/rubyonrailstutor/curriculum
screencast: "//www.youtube.com/embed/WM9OeZnunno?vq=hd1080"
comments: true
---

```
# http://ruby-doc.org/core-2.1.1/Hash.html
# join a social pair programming class http://www.rubyonrailstutor.com

people = { john: "davison", mike: "the mechanic", sally: "fields"}

people[:john]

# why does "first" only get printed once ? 
people = { first: "john", last: "davison", first: "mike", last: "the mechanic" }
people

# what is the element ':first' called ? 

person = { first: "john", last: "davison" }
person[:first].class

nested_hash = { people: { coders: ["john davison", "mike the mechanic", "sally fields"], athletes: ["jordan", "kobe", "canseco"]}, places: "monte carlo, milan, tahiti"}

people = person.keep_if {|key, value| key == :people}

# join a social pair programming class http://www.rubyonrailstutor.com
```
