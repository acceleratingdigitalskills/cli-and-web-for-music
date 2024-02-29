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

The majority of users access web resources by using browsers, such as Google Chrome, Mozilla Firefox, and Apple’s Safari, to view and interact with websites. Remote computers deliver the content of websites, via the internet, to the users’s computer following a request from the browser. In this course, we don’t have time to describe the details of how this content is delivered. However, It is important to know the following terminology:

- server: a computer connected to the internet that provides content on request
= client: a computer connected to the internet that requests and receives content

Usually, the user deliberately makes these requests from the browser either by directly typing in the location of the content that is being requested into the browser’s navigation bar, or, more frequently, by clicking on hyperlinks, or links. The browser then uses a set of rules (shared by the client and the server) to initiate the request, and handle the response. 

![An illustration of what happens when a user "visits" a web page using a browser](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/b450e56f-d4c7-4b01-b26f-cca30fbeac15)

A set of rules regulating the communication between two parties is called a protocol. The most commonly used set of rules has been specified over the last several decades of its existence and is called HTTP, which stands for HyperText Transfer Protocol. HTTP provides a set of formal guidelines about how Web content is published and made available on a server, and how a client should make and handle requests for this content. 

The set of rules or patterns that specify the form the data that is passed between two parties is called a file format. You are likely familiar with a selection of file formats already. For example, the difference between a `.doc` file and a `.pdf` file of the same final-year essay is primarily a difference of format. One file format that is commonly requested by and delivered to web users is HyperText Markup Language, or HTML (`.html` file extension).

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


::::::::::::::::::::::::::::::::::::: challenge 

## Challenge 2: The feel of the web

1. Pick a website that you regularly consult for research purposes; any website will do
2. Visit any page on this website
3. Open the developer tools in your browser and navigate to the Network tab (the name may vary). Press the refresh button (or F5)

Post your answer to the following questions:

1. The URI of the page or resource on the site that you visited
2. A URI pointing to a CSS file (ending .css) used by this page
3. A URI pointing to a Javascript file (ending .js) used by this page
4. A URI pointing to an image file (many extensions possible) used by this page
5. A URI pointing to some other file (many extensions) used by this page

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

