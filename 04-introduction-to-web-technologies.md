---
title: "Introduction to Web technologies"
teaching: 15
exercises: 10
---

:::::::::::::::::::::::::::::::::::::: questions

- How do browsers retrieve and display websites from remote servers?
- How is the structure and content of a web page reflected in code? 
- How can I specify the location of a website or other resource on a remote server?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- To know that HTTP is used to request remote resources by browsers and by other applications
- To understand that browsers make multiple HTTP requests when loading most modern websites
- To understand the important components of a URL

::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: instructor

Instructor notes

::::::::::::::::::::::::::::::::::::::::::::::::

## What is a URL?

A URL can be thought of as a path to a resource on a remote server, which is nothing more than a way to access data on someone else's computer. A "resource" maybe a web page, a media file, an entire site, a folder, or even a more complicated interactive experience. 

URLs have some obvious similarities with paths, in that the forward slash character (`/`) is used as a path separator. Howeer, there is no guarantee that the structure of the URL corresponds directly to some filesystem hierarchy in the remote server.

There are also some additional elements to URLs that distinguish them from paths.

:::::::::::::::::::::::::::::::::::::::::  callout

## Absolute vs. relative URLs

Just like with paths, there are absolute URLs and relative URLs. This distinction is not relevant for the rest of this lesson, but if you would like to learn more about this, please consult the [mdn web docs page, "What is a URL?"](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL).

::::::::::::::::::::::::::::::::::::::::::::::::::

