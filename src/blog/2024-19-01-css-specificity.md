---
title: CSS Specificity
author: Ekaterina Furman
date: 2024-01-19
tags: ["post", "featured"]
image: /assets/blog/css-specificity.jpg
imageAlt: css specificity counters
description: What is CSS selector specificity and how does it work? Specificity is an algorithm that calculates the weight that is applied to a given CSS declaration.
---

What is CSS selector specificity and how does it work?

### General Overview:

Each selector rule gets a scoring. You can think of specificity as a total score and each selector type earns points towards that score. The selector with the highest score wins.

With specificity in a real project, the balancing act is making sure the CSS rules you expect to apply, actually do apply, while generally keeping scores low to prevent complexity. The score should only be as high as we need it to be, rather than aiming for the highest score possible. In the future, some genuinely more important CSS might need to be applied. If you go for the highest score, you'll make that job hard.

### Scoring The Selector Types

**Universal selector ( \* )**<br>
This selector has no specificity and gets 0 points. Meaning that any rule with 1 or more points will override it.

**Type or Psuedo-Element selector ( div, span, p, ::before)**<br>
These elements get 1 point.

**Class, Psuedo-Class, or Attribute selector ( .my-class, :hover, a[attr="value"])**<br>
Each of these will get 10 points.

Sidenote: the :not() pseudo-class itself adds nothing to the specificity calculation. However, the selectors passed in as arguments do get added to the specificity calculation.<br>

<code>
div:not(.my-class) {<br>
color: red;<br>
}<br>
</code>

This sample would have 11 points of specificity because it has one type selector (div) and one class inside the :not()

**ID Selector ( #myID )**<br>
An ID selector gets 100 points of specificity, as long as you use an ID selector (#myID) and not an attribute selector ([id="myID"])

**Inline Style Attribute**<br>
CSS applied directly to the style attribute of the HTML element, gets a specificity score of 1,000 points. This means that in order to override it in CSS, you have to write an extremely specific selector.

**!important rule**<br>
Lastly, an !important at the end of a CSS value gets a specificity score of 10,000 points. This is the highest specificity that one individual item can get.

An !important rule is applied to a CSS property, so everything in the overall rule (selector and properties) does not get the same specificity score.

<code>
.my-class {<br>
  color: red !important; /* 10,000 points */<br>
  background: white; /* 10 points */<br>
}<br>
</code>
