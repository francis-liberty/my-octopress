---
layout: post
title: "Half way in Java"
date: 2014-11-03 22:20:01 +0800
comments: true
categories: Java
---

Because I need to learn some MR stuff, I'm now half way in Java again ... Never truely learned Java. 

<!-- more -->

It costs me hours to come up that Java class uses full path name to refer to a main class, like ```hadoop ch.shuo.mr.MainClassName input output -jarlibs=./target/sample-1.0.jar```

## String Manipulation
* like Python join() function
``` java
	public static String join(String[] list, String delim) {
		/* like Python join() function
		*/

    StringBuilder sb = new StringBuilder();
    String loopDelim = "";

    for(String s : list) {
        sb.append(loopDelim);
        sb.append(s);       

        loopDelim = delim;
    }

    return sb.toString();
	}
```

## Array Manipulation
* like Python [n:]
``` java
  import java.utils.Arrays
	Arrays.copyOfRange(arr, n, arr.length);
```