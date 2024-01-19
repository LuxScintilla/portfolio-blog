---
title: HTML Cookies and Storage
author: Ekaterina Furman
date: 2024-01-18
tags: ["post", "featured"]
image: /assets/blog/html-storage.jpg
imageAlt: This is a test
description: Describe the difference between a cookie, sessionStorage and localStorage.
---

<p>Describe the difference between a cookie, sessionStorage and localStorage.</p>

### General Overview:

The local storage is a type of HTML5 offline storage that allows user string data to be saved synchronously in their browser. Information is kept in name and value pairs and not available between different browsers on the same device.

Local storage can be used as an alternative to cookies. It provides a chance to store more data: 4KB is the limit for cookies, and local storage allows using up to 10MB, depending on the browser. Moreover, the process is more efficient – the browser does not send any local storage data to the server in any step.

### Local Storage:

Most web applications these days require some type of user input, whether it be for a username, shipping address, or even just a preferences setting. This input is then usually sent off to a server somewhere to be processed and stored. However, what if your application needs to store data locally on the user’s computer? This is where Local Storage comes in.

Local Storage is a type of web storage that allows JavaScript to store and access data right in the browser. This is especially useful for storing data that you want to persist even if the user closes the browser, such as preferences or settings.

The data in Local Storage is stored in key/value pairs. The key is like the name of the data, and the value is like the actual data itself. You can think of it as a variable in JavaScript. To store data in Local Storage, you first need to create a key. Then you can store any data you want under that key.

To create a key, you use the setItem() method. This method takes two arguments, the first is the key, and the second is the value you want to store.

<code>
localStorage.setItem('key', 'value');
</code>

Now that you have a key, you can store any data you want under that key. The data you store can be any data type that JavaScript supports, including strings, numbers, objects, and arrays.

To store data, you use the setItem() method again. This time, you pass in the key as the first argument and the data you want to store as the second argument.

<code>
localStorage.setItem('key', 'value');
</code>

To retrieve data from Local Storage, you use the getItem() method. This method takes the key as an argument and returns the data that is stored under that key.

<code>
localStorage.getItem('key');
</code>

If you want to remove an item from Local Storage, you use the removeItem() method. This method takes the key as an argument and removes the data that is stored under that key.

<code>
localStorage.removeItem('key');
</code>

### Session Storage:

The sessionStorage object stores data only for a session. It means that the data stored in the sessionStorage will be deleted when the browser is closed.

A page session lasts as long as the web browser is open and survives over the page refresh.

When you open a page in a new tab or window, the web browser creates a new session.

If you open multiple tabs or windows with the same URL, the web browser creates a separate sessionStorage for each tab or window. So data stored in one web browser tab cannot be accessible in another tab.

When you close a tab or window, the web browser ends the session and clears data in the sessionStorage.

Data stored in the sessionStorage is specific to the protocol of the page. For example, the same site javascripttutorial.net has different sessionStorage when accessing with the http and https.

Since the sessionStorage data is tied to a server session, it’s only available when a page is requested from a server. The sessionStorage isn’t available when the page runs locally without a server.

Because the sessionStorage is an instance of the Storage type, you can manage data using the Storage’s methods:

<ul>
  <li>setItem(name, value) – set the value for a name</li>
  <li>removeItem(name) – remove the name-value pair identified by name</li>
  <li>getItem(name) – get the value for a given name</li>
  <li>key(index) – get the name of the value in the given numeric position</li>
  <li>clear() – remove all values in the sessionStorage</li>
</ul>

Just like cookies, HTML5 offline storage shouldn't be used to store sensitive information (e.g., user IDs or payment information). It can be easily accessed by any JS script and compromised in case of a cross-scripting attack.

### Cookies:

An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to a user's web browser. The browser may store the cookie and send it back to the same server with later requests. Typically, an HTTP cookie is used to tell if two requests come from the same browser—keeping a user logged in, for example. It remembers stateful information for the stateless HTTP protocol.

Cookies are mainly used for three purposes:

<ul>
  <li>Session management:
  Logins, shopping carts, game scores, or anything else the server should remember</li>
  <li>Personalization:
  User preferences, themes, and other settings</li>
  <li>Tracking:
  Recording and analyzing user behavior</li>
</ul>

### Conclusion:

**Cookies:**

  <ul>
    <li>Capacity: 4KB</li>
    <li>Access: Any Window</li>
    <li>Expiration: Set Manually</li>
    <li>Location: Browser and Server</li>
    <li>Sent with Requests: Yes</li>
  </ul>

**Local Storage:**

  <ul>
    <li>Capacity: 10MB</li>
    <li>Access: Any Window</li>
    <li>Expiration: Never</li>
    <li>Location: Browser</li>
    <li>Sent with Requests: No</li>
  </ul>

**Session Storage:**

  <ul>
    <li>Capacity: 5MB</li>
    <li>Access: Same Tab</li>
    <li>Expiration: on Tab or Window close</li>
    <li>Location: Browser</li>
    <li>Sent with Requests: No</li>
  </ul>
