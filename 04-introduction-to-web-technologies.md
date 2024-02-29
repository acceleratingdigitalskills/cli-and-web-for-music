---
title: "Introduction to Web technologies"
teaching: 15
exercises: 10
---

:::::::::::::::::::::::::::::::::::::: questions

- How do browsers retrieve and display websites from remote servers?
- How and where are the structure and content of a web page located in code? 
- How do I specify the location of a website or other resource on a remote server?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- To know that HTTP is used to request remote resources by browsers and by other applications
- To understand that browsers make multiple HTTP requests when loading most modern websites
- To understand the important components of a URL

::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: instructor

Learners should be familiar with paths and file extensions. This episode asks learners to use a web broswer.

::::::::::::::::::::::::::::::::::::::::::::::::

## What happens when we use a web browser?

## What is a URL?

A URL can be thought of as a path to a resource on a remote server, which is nothing more than the location of data on someone else's computer. A "resource" may be a web page, a media file, an entire site, a folder, or even a more complicated interactive experience. The following are examples of URLs:

- http://rte.ie
- https://www.eamonnbell.com/blog/2020/11/15/ams-broken-light-2020/
- https://duckduckgo.com/?q=discogs.com&ia=web
- https://www.discogs.com/sell/item/1969451180

URLs have some obvious similarities with paths. For example, the forward slash character (`/`) is used as a separator. This helps keep web resources organised, but can also help researchers, as we will see in later episodes. Howeer, there is no guarantee that the structure of the URL corresponds directly to the layout of particular directories on the remote server.

There are also some additional elements to URLs that distinguish them from paths. Let's have a look at the anatomy of a URL:

![The anatomy of a URL (credit: mdn Web docs)](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/dd152a76-cae4-4839-821d-0690aecfd33b){alt='A sample URL with its components highlighted: scheme, domain name, port, path, parameters, and anchor'}

- *scheme*: tells what protocol should be used to interact with the remote resource
- *domain name*: points us to the location of the remote server in human-readable form
- *port*: an integer that is used to further specify where to look on the remote server 
- *path*: where the remote resource is located within the organisational structure of the server
- *parameters*: a list of key-value pairs, separated by the `&` symbol which modify the resource returned in some way
- *anchor*: this optional part of a URL can be used to link directly to some component  

::::::::::::::::::::::::::::::::::::: challenge 

## Challenge 1: Dissecting a URL

Study the following URL

- https://duckduckgo.com/?q=discogs.com&ia=web

and post your answer to the following questions:

1. What is the scheme?
2. How many domains are in the URL?
3. Is there a port specified in this URL?
4. What is the value associated with the second key in URL parameters?

:::::::::::::::::::::::: solution 

1. https (Secure HTTP/TLS)
2. One: `duckduckgo.com`. (`discogs.com` is in the URL parameters; arbitrary strings may appear here - potentially even including whole URLs)
3. There is not. However, different schemes have default ports associated with them which will be used by applications when no port is specified explicitly.
4. `web`

:::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::



:::::::::::::::::::::::::::::::::::::::::  callout

## Absolute vs. relative URLs

Just like with paths, there are absolute URLs and relative URLs. This distinction is not relevant for the rest of this lesson, but if you would like to learn more about this, please consult the [mdn web docs page, "What is a URL?"](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL).

::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints

- HTTP
- URIs
- Developer tools can be used
::::::::::::::::::::::::::::::::::::::::::::::::

