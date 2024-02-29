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

There are also some additional elements to URLs that distinguish them from paths. Let's have a look at the anatomy of a URL

![The anatomy of a URL (credit: mdn Web docs)](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/dd152a76-cae4-4839-821d-0690aecfd33b){alt='A sample URL with its components highlighted: scheme, domain name, port, path, parameters, and anchor'}


::::::::::::::::::::::::::::::::::::: challenge 

## Challenge 1: Can you do it?

What is the output of this command?

```r
paste("This", "new", "lesson", "looks", "good")
```

:::::::::::::::::::::::: solution 

You should find a variety of files here.
 
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

