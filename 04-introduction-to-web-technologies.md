---
title: "Introduction to Web technologies"
teaching: 20
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

Learners should be familiar with paths and file extensions. This episode asks learners to use a web browser.

::::::::::::::::::::::::::::::::::::::::::::::::


## What happens when we use a web browser?

The majority of users access web resources by using browsers, such as Google Chrome, Mozilla Firefox, and Apple’s Safari, to view and interact with websites. Remote computers deliver the content of websites, via the internet, to the users’s computer following a request from the browser. In this course, we don’t have time to describe the details of how this content is delivered. However, It is important to know the following terminology:

- *server*: a computer connected to the internet that provides content on request
- *client*: a computer connected to the internet that requests and receives content

Usually, the user deliberately makes these requests from the browser either by directly typing in the location of the content that is being requested into the browser’s navigation bar, or, more frequently, by clicking on hyperlinks, or links. The browser then uses a set of rules (shared by the client and the server) to initiate the request, and handle the response. 

![An illustration of what happens when a user "visits" a web page using a browser](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/b450e56f-d4c7-4b01-b26f-cca30fbeac15)

A set of rules regulating the communication between two parties is called a protocol. The most commonly used set of rules has been specified over the last several decades of its existence and is called HTTP, which stands for HyperText Transfer Protocol. HTTP provides a set of formal guidelines about how Web content is published and made available on a server, and how a client should make and handle requests for this content. It is a relatively straightforward protocol, using a set of "verbs" that specify the actions that the client wishes to communicate to the server. One such verb is `GET`, which is why this appears in the diagram above.

The set of rules or patterns that specify the form the data that is passed between two parties is called a file format. You are likely familiar with a selection of file formats already. For example, the difference between a `.doc` file and a `.pdf` file of the same final-year essay is primarily a difference of format. One file format that is commonly requested by and delivered to web users is HyperText Markup Language, or HTML (`.html` file extension). 

We will look more closely at the HTML format in a subsequent episode. For now, you can think of the HTML format as providing a way to specify (a) the content of a document (i.e. what text, images, and other media - if any - should it consist of) alongside (b) the logical structure of the document (i.e. any hierarchical aspects that structure these contents relative to each other, such as a title, headings, and subheadings, and/or other part-whole relationships).

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
- *anchor*: this optional part of a URL can be used to link directly to some component of the file being requested, typically a header or subheader of a HTML document

::::::::::::::::::::::::::::::::::::: challenge 

### Challenge 1: Dissecting a URL

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


## Content vs. styling: HTML and friends

Web browsers are little more than glorified document fetchers and viewers for the web. The main reason that browsers do not seem quite like this is because these documents have become highly interactive, and because web designers have moved to a mode of designing websites and web applications so that they increasingly resemble the kinds of graphical applications that run on your desktop computer (with icons, menus, toolbars, animations/transitions, etc.) The earliest websites were much less interactive. Yet, no matter how complicated or simple the design of a website, every single piece of content in a web page - starting with textual content and the logical strucutre of the page itself -  must be fetched by the browser. We have already learned that format used to encode this content is called HTML, and is associated with the file extension `.html`.

Next, we consider the overall look and feel or "style" of the website. Aspects of styling may include the size, color, and font choices for the text but also other considerations such as the relative or absolute layout of key page elements and their size. This information is conventionally transferred from the server to the browser as a separate file or set of files, in a format called Cascading Style Sheets (or, CSS), and is associated with the `.css` file extension. In order for the browser to present the web resource as intended, another HTTP request is required to retrieve the appropriate CSS file(s). Since HTTP makes use of URLs to locate and retrieve resources, there will be a URL associated with each of these files.

![](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/e0460463-5dee-45e5-a723-09f21b10f2e3)

The web is a multimedia platform, and one of the earliest media types to be supported by browsers was the image. As you may know, images may be stored in a variety of formats (e.g. GIF, JPEG, WebP), and there is therefore a variety of extensions associated with them (i.e. `.gif`, `.jpg` or `.jpeg`, `.webp`). Again, for each image, a new HTTP request is typically required. Hence, each image will likely be associated with its own URL. You may notice that the URLs for resources, such as images, do not necessarily contain the same domain name as the domain name of the site you are visiting.

![](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/8a54d646-d044-434a-9fc0-3873686d178c)

Increasingly, designers are keen to ensure that websites and related resources are interactive and dynamic, and this requires the transfer of content in yet another format: Javascript. Javascript is a flexible, general-purpose programming language that is executed (more-or-less) entirely contained within the browser and allows web developers to create extremely rich, interactive modifications to the document content on the fly. It is commonly stored in files with the `.js` extension, which are requested by the browser, again using HTTP.

![](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/b7794a69-c650-4196-82ed-6072bf3616af)

Once the assorted files have been requested by the client, which in this case is the web browser, they are assembled and interpreted to provide the total experience of the page. The specific details of each of thes file formats are not relevant to this lesson; the key takeaway is that most web pages in fact decompose into multiple parts, each of which is associated with a single HTTP request. Understanding this fact allows us to begin to pick apart web resources into their consituent parts, some of which are more or less usable for research purposes.

## Developer Tools and the complexity of the modern web

To understand precisely what and how many HTTP requests that a browser makes in the course of requesting a single web page, we can use the built-in Developer Tools function of most modern borwsers, to inspect the all network activity for a single page load event.

Most modern browsers include a set of tools called "developer tools", which areused by the programmers who create websites and other interactive experiences to debug and assess the performance of their creations, among other things. However, they are an extraordinarily useful asset for researchers, and are a useful way to get started thinking about what's "under the hood" of the web. These are almost certainly available in the browser you've already installed.

:::::::::::::::::::::::::::::::::::::::::  callout

### Developer tools in different browsers

Different browsers (and different operating systems) expose developer tools in different ways. Here is a quick guide. Some of the details of what follows will vary depending on your specific browser. To follow along exactly, it is recommended to use Google Chrome.

#### Microsoft Edge
1. Click on the **three-dot menu** in the top right corner.
2. Hover over **More Tools**.
3. Click on **Developer Tools**.

Or simply use the shortcut <kbd>F12</kbd> or <kbd>Ctrl+Shift+I</kbd> on your keyboard.

#### Firefox
1. Click on the **three-line menu** in the top right corner.
2. Click on **Web Developer**.
3. Click on **Toggle Tools**.

Or simply use the shortcut <kbd>F12</kbd> or <kbd>Ctrl+Shift+I</kbd> on your keyboard.

#### Google Chrome
1. Click on the **three-dot menu** in the top right corner.
2. Hover over **More Tools**.
3. Click on **Developer Tools**.

Or simply use the shortcut <kbd>F12</kbd> or <kbd>Ctrl+Shift+I</kbd> on your keyboard.

#### Safari (on Mac)
1. Click on **Safari** in the top left corner of the screen.
2. Click on **Preferences**.
3. Go to the **Advanced** tab.
4. Check the box at the bottom that says **Show Develop menu in menu bar**.
5. Close the Preferences window. The **Develop** menu will now appear in the menu bar.
6. Click on **Develop** in the menu bar.
7. Click on **Show Web Inspector**.

Or simply use the shortcut <kbd>Cmd+Option+I</kbd> on your keyboard.

::::::::::::::::::::::::::::::::::::::::::::::::::

To do this:

1. First, navigate to a site of your choice
2. Then, open Developer Tools using the three dots menu in the top right (Windows/Linux) or under the menu View > Developer... (or <kbd>Ctrl+Shift+I</kbd>/<kbd>Cmd+Shift+I</kbd>)
3. A new pane will pop open; navigate to the “Network” pane.
4. Ensure that network activity is being recorded by clicking the red “record” button in the top left of the pane
5. Refresh the page (shortcut: F5)
6. Once the page is finsihed loading, disable recording

Something like the image shown here will result:

![](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/dbc8f0be-55a1-4963-bad0-c9c0d4cd3a59)

The colored bars at the top of the screen show each individual HTTP request graphically (the “waterfall”), with the duration taken for each request to be fulfilled is given by the length of the bar. The different colors indicate what the status of the request is over time. Notice also the statisics at the end of the file list: the total number of requests made, the total amount of data transferred, and the total load time for the site.

To dig into a particular request, select it from the list and double click on it. It will open a new pane as below. Look at the very first request in the list, the request for the document itself: index.html. From this we’ll see a a lot more information about the request, including the HTTP status code associated with the response, and the IP address of the responding server. We also see the request method, the HTTP “verb” that was used to fetch the resource. Almost all browser-initated requests will use the `GET` verb, but others are available (`POST` is another verb and is used to submit form data, and sometimes to call APIs — see later episodes).

Under the Timing pane, you’ll see a more fine-grained look at the time that each request took and what the colors stand for.

![](https://github.com/acceleratingdigitalskills/cli-and-web-for-music/assets/94374319/4c87eaa7-03a0-4359-ab40-4e1abddf92fd)

::::::::::::::::::::::::::::::::::::: challenge 

### Challenge 2: The feel of the web

1. Pick a website that you regularly consult for research purposes; any website will do
2. Visit any page on this website
3. Open the developer tools in your browser and navigate to the Network tab (the name may vary). Press the refresh button (or F5)

Post your answer to the following questions:

1. The URL of the page or resource on the site that you visited
2. A URL pointing to a CSS file (ending .css) used by this page
3. A URL pointing to a Javascript file (ending .js) used by this page
4. A URL pointing to an image file (many extensions possible) used by this page
5. A URL pointing to some other file (many extensions) used by this page

::::::::::::::::::::::::::::::::::::::::::::::::


:::::::::::::::::::::::::::::::::::::::::  callout

### Absolute vs. relative URLs

Just like with paths, there are absolute URLs and relative URLs. This distinction is not relevant for the rest of this lesson, but if you would like to learn more about this, please consult the [mdn web docs page, "What is a URL?"](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL).

::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints

- Web servers provide remote resources to clients, most commonly browsers, using the HTTP protocol
- URLs are the "addresses" of the web, and they specify the location of a remote resource for the purposes of retrieval
- Most websites today consist of resources of a variety of file formats, and each remote resource usually demands its own HTTP request and has its own URL associated with it 
- We can inspect the torrent of HTTP requests that websites require by using most modern browser's Developer Tools

::::::::::::::::::::::::::::::::::::::::::::::::

