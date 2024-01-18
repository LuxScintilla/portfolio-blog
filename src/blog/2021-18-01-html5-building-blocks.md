---
title: HTML5 Building Blocks
author: Ekaterina Furman
date: 2024-01-18
tags: ["post", "featured"]
image: /assets/blog/html5-building-blocks.jpg
imageAlt: html5 code
description: Consider HTML5 as an open web platform. What are the building blocks of HTML5?
---

Consider HTML5 as an open web platform. What are the building blocks of HTML5?

### Key Elements:

<ul>
  <li>Semantic Structure</li>
  <li>Multimedia Support</li>
  <li>Canvas</li>
  <li>Scalable Vector Graphics (SVG)</li>
  <li>Offline Storage</li>
  <li>Enhanced Forms</li>
</ul>

### General Overview:

HTML5 is a markup language that provides a rich set of features for building web applications. Its building blocks consist of several essential components. Firstly, HTML5 emphasizes semantic structure, allowing developers to use meaningful tags and elements to describe the content, enhancing accessibility and search engine optimization. Secondly, HTML5 provides native support for multimedia, including audio and video elements, eliminating the need for third-party plugins like Flash. Additionally, the canvas element enables dynamic rendering and manipulation of graphics and animations using JavaScript. HTML5 also incorporates Scalable Vector Graphics (SVG) for high-quality resolution-independent graphics. It offers offline storage capabilities, allowing web applications to store data locally and work offline. Finally, HTML5 introduces enhanced form elements, such as new input types, form validation, and date pickers, improving user experience and simplifying form handling.

Collectively, these building blocks of HTML5 contribute to its versatility, interactivity, and multimedia capabilities, enabling developers to create engaging web applications and experiences.

### What Is Semantic Structure:

Semantic HTML, also known as semantic markup, refers to the use of HTML tags that convey the meaning—or semantics—of the content contained within them.
By adding semantic HTML tags to your pages, you provide additional information that helps define the roles and relative importance of the different parts of your page.

For example, **header**, **section**, **article**, and **footer**. These are semantic HTML tags. They clearly indicate the role of the content they contain.
On the other hand, tags like **div** and **span** are typical examples of non-semantic HTML elements. They serve only as content holders but give no indication as to what type of content they contain or what role that content plays on the page.

Besides the obvious reason that semantic HTML tags are easier to read and understand—for example, by web developers reviewing the code—there are two more specific reasons why you should always use semantic tags.

Accessibility, it is not that easy for users who are blind or visually impaired and rely on screen readers. The proper use of HTML semantic tags will allow these readers to understand your content better because their screen readers will communicate your content more accurately.

Semantic HTML tags are important for SEO (search engine optimization) because they indicate the role of the content within the tags. That information gives search engine crawlers, like Googlebot, a better understanding of your content. This increases the chances that your content will be selected as a candidate for ranking on the search engine results page (SERP) for relevant keywords.

### Multimedia Tags:

HTML allows adding different multimedia files on your website by various multimedia tags. These tags include:

<ul>
  <li>audio</li>
  <li>video</li>
  <li>embed</li>
  <li>object</li>
  <li>iframe</li>
</ul>

### What Is HTML5 Canvas:

The Canvas API provides a means for drawing graphics via JavaScript and the HTML canvas element. Among other things, it can be used for animation, game graphics, data visualization, photo manipulation, and real-time video processing.

The Canvas API largely focuses on 2D graphics. The WebGL API, which also uses the canvas element, draws hardware-accelerated 2D and 3D graphics.

### What Are SVG's:

Scalable Vector Graphics (SVG) is an XML-based markup language for describing two-dimensional based vector graphics.

As such, it's a text-based, open Web standard for describing images that can be rendered cleanly at any size and are designed specifically to work well with other web standards including CSS, DOM, JavaScript, and SMIL. SVG is, essentially, to graphics what HTML is to text.

SVG images and their related behaviors are defined in XML text files, which means they can be searched, indexed, scripted, and compressed. Additionally, this means they can be created and edited with any text editor or with drawing software.

Compared to classic bitmapped image formats such as JPEG or PNG, SVG-format vector images can be rendered at any size without loss of quality and can be easily localized by updating the text within them, without the need of a graphical editor to do so. With proper libraries, SVG files can even be localized on-the-fly.

### What Is HTML Offline Storage:

With web storage, web applications can store data locally within the user's browser.

Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.

Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.
Web storage is per origin (per domain and protocol). All pages, from one origin, can store and access the same data.
HTML web storage provides two objects for storing data on the client:

<ul>
  <li>window.localStorage - stores data with no expiration date</li>
  <li>window.sessionStorage - stores data for one session (data is lost when the browser tab is closed)</li>
</ul>

### What Are Enhanced Forms:

Forms are used everywhere on the web to accept the data from the user and process the information from the submitted data. However, before submitting any data to the server, it's essential to check whether the user entered the data in the correct format. This is also called client-side validation because it helps ensure the submitted data is in proper form on the client side.

With the dawn of HTML5, a raft of new input types and attributes were added to **input** tags that allow the browsers themselves to perform the client-side validation for us: no JavaScript required. To start using the new input types and attributes, you don't really need to do anything other than start using the new input types and attributes, such as **required**, **placeholder**, **type**, **pattern** attributes, and many many more.

### Conclusion:

If you ask this question to anybody, you will likely get many varying answers. This is because HTML5 introduced many new features, aside from the ones already mentioned, such as Responsive Images, Geolocation API, Drag and Drop API, Web Sockets and Micro Data. But if you go back to the very basics of HTML, you would end up with **tags**, **elements** and **attributes**.
