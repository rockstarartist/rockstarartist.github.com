---
layout: post
title:  "Learning ECMA6"
date:   2015-07-20 16:23:00
categories: javascript ecma6 oscon2015
---

So I am at OSCON 2015 in Portland, Oregon. After flight delays, and rebooking my flight and arriving late and missing my
first full day session, I was able atleast to enter the tail end of a session on react.js with ES6. I am surprised at how
quickly facebook just jumped on ES6 and started using it for the applications and frameworks.

A couple things I learned about react:


- JSX by convention reads lowercase tags as real HTML tags, and uppercase starting tags are assumed to be react components.
- A rule of thumb, in regards to handling events, always handle the events inside the same components, makes it easier to
extend the component. So you change the props of the user selection inside this eventhandler, and you then set a listener
on the parent component, which then sets the state, and react rerenders the component.

So what do I need to do? I need to do at least one ECMA6 code piece everyday to get good and become knowledgeable on ECMA6.

