---
layout: post
title:  "Welcome to RockStarArtist!"
date:   2015-05-27 14:43:36
categories: firstpost update
---
First post.

I am hoping to begin a repository, a memory map of sorts, conceived of learned lessons and massive failures. To jot
down things in which I will fail to recall later on, or materials that I deem of worthy nature and may return to in 
the near future.

This is a little java library that I created to show `code snippets` in jekyll:

{% highlight js %}
window.Utils = (function(){
    var utils = {
        /**
         * Similar to the indexOf method of an array. In this case, you provide the array,
         * the attribute that you want to check, the value of the attribute, and optionally
         * a start index value. This function will return the index of the object that
         * contained the specified attribute's value, and if an object that meets that
         * criteria is not found, the function returns an "undefined" object type.
         * 
         * @param {Array} array The array that you are searching through.
         * @param {String} attr The attribute that you are searching for.
         * @param {Object} value The value of the attribute that you are searching for.  This can be
         *      anything (String, Number, Truthy, anything that could be a value of a js Object).
         * @param {Number} startindex The starting index of where you want the search to begin from.
         * @returns {Number} Returns an integer or undefined object type.
         */
        indexOfAttr: function(array, attr, value, startindex) {        
            if (typeof startindex === "undefined") {        
                startindex = 0;     
            }       
            for (var i = startindex; i < array.length; i += 1) {        
                if (array[i][attr] === value) {     
                    return i;       
                }       
            }       
        },
        /**
         * Function that transforms a javascript data object into a time stamp
         * that includes month and day.
         * 
         * @param {Number} A Unix timestamp.
         * @returns {String} Time as a string in the format of MM/DD HH:MM:ss am/pm
         */
         getPrettyTimestamp: function(t) {
            var time = new Date(t);
            var month = time.getMonth();
            var day = time.getDate();
            var hour = time.getHours();
            var minutes = time.getMinutes();
            var seconds = time.getSeconds();
            if (minutes < 10) {
                minutes = "0" + minutes;
            }
            if (seconds < 10) {
                seconds = "0" + seconds;
            }
            var ampm = "am";
            if (hour === 0) {
                hour = 12;
            } else if (hour > 12) {
                ampm = "pm";
                hour = hour - 12;
            } else if (hour === 12) {
                ampm = "pm";
            }
            return month + "/" + day + " " + hour + ":" + minutes + ":" + seconds + " " + ampm;
        },
        /**
         * Function that transforms a javascript data object into a time stamp.
         * 
         * @param {Number} t A Unix timestamp.
         * @returns {String} Time as a string in the format of HH:MM:ss am/pm
         */
        getShortTimestamp: function(t) {
            var time = new Date(t);
            var hour = time.getHours();
            var minutes = time.getMinutes();
            var seconds = time.getSeconds();
            if (minutes < 10) {
                minutes = "0" + minutes;
            }
            if (seconds < 10) {
                seconds = "0" + seconds;
            }
            var ampm = "am";
            if (hour === 0) {
                hour = 12;
            } else if (hour > 12) {
                ampm = "pm";
                hour = hour - 12;
            } else if (hour === 12) {
                ampm = "pm";
            }
            return hour + ":" + minutes + ":" + seconds + ampm;
        }
    };
    return utils;
})(); 
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

