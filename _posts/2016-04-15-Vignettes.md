---
layout: post
title: Vignettes in R packages
date: "2016-04-15"
tags: 
  - R
---

I find it very useful to go through vignettes provided by R packages, which help me figure out how to use the functions within them. For example, the package "dismo", has a useful vignette names "sdm", for species distribution modeling. 

We use the function `vignette` and `edit` to go about this. 

For example, 
{% highlight r %}

# Vignettes within dismo package
vignette(package = "dismo")

# Opening "sdm" vignette
vignette("sdm", package = "dismo")

# Editing and going through the vignette code
edit(vignette("sdm", package = "dismo"))

# or
v = vignette("sdm", package = "dismo")
edit(v)

# Viewing vignette
print(v)

# Listing vignettes from all attached packages
vignette(all = FALSE)

# Listing vignettes from all installed packages
vignette(all = TRUE)

{% endhighlight %}

Thanks to this [post](http://www.inside-r.org/r-doc/utils/vignette) from [inside-R](http://www.inside-r.org/), which provided an excellent reference when I was searching how to do it.  
