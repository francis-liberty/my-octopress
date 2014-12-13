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

* ListArray<String> to String[]
``` java
    List<String> list =new ArrayList<String>();
    //add some stuff
    list.add("android");
    list.add("apple");
    String[] stringArray = list.toArray(new String[list.size()]);
```

## Array Manipulation
* like Python [n:]
``` java
    import java.utils.Arrays
	Arrays.copyOfRange(arr, n, arr.length);
```

* convert from arraylist to array
``` java
    ArrayList<Integer> arrlist = new ArrayList<Integer>();
    // use add() method to add values in the list

    Integer list2[] = new Integer[arrlist.size()];
    list2 = arrlist.toArray(list2);
```

* sort
``` java
    import java.util.Collections;
    Collections.sort(arrList);
```

## Map Manipulation

* iterate
``` java
    for (Integer k: m.keySet())
```

## File Manipulation

* read a file line by line
``` java
    BufferedReader br = new BufferedReader(new FileReader(file));
    String line;
    while ((line = br.readLine()) != null) {
       // process the line.
    }
br.close();
```