---
title: "Go Maps"
date: 2017-06-27T09:27:36+01:00
draft: false
---

This is a bit of a Tuesday micro-blog looking at the performance of various solutions for concurrent map insertion/retrieval in golang.

In particular I'm going to look at three types of Map:

1. Go's builtin map type, protected by a read-write mutex (sync/atomic/RWMutex)
2. Go's new sync.Map type, which is an optimized scalable concurrent map.
3. Go's builtin map type, protected by an elided rw-mutex.

{{< highlight go "linenos=inline,hl_lines=2 3" >}}
var a string
var b string
var c string
var d string
{{< / highlight >}}





