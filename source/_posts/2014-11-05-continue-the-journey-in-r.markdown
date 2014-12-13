---
layout: post
title: "continue the journey in R"
date: 2014-11-05 23:19:04 +0800
comments: true
categories: 
---

* change locale
``` R
Sys.setlocale("LC_ALL", 'en_US.UTF-8')
```

* iterate all files under a directory
``` R
files <- list.files(path="./16_excels", pattern="*.xlsx", full.names=T, recursive=FALSE);
lapply(files, function(file) {
});
```

## data.frame

* convert a data frame column to numeric type
``` R
	transform(d, fake_char = as.numeric(fake_char), 
	               char_fac = as.numeric(char_fac))
```

## xlsx
* to increase java Heap size(sufficient)

``` R
options(java.parameters = "-Xmx1000m")
```