---
layout: post
title: "Building your own R packages"
date: "2016-05-01"
tags:
 - R
 publish: no
---
Under construction

I made this post for a short talk on building and documenting your own R packages for the Davis R-users' group. It'll get you started on making basic R packages, and once you get the flavor of what it's all about, you can unleash your own inner R genie to create your own tools!

![]({{ nistara.github.io }}/_assets/images/R genie.png)

<br><br>
The tools you're going to need for this are:

- Git and github - [Karl Broman](http://kbroman.org/github_tutorial/pages/first_time.html) has succinct instructions for getting started with both. 

- R packages
    * devtools - to easily create and publish your package on github
    * roxygen2 - for easy documentation of your package

### Let's get started

First, create your package in the directory you want it to be:


{% highlight r %}
devtools::create("demo")
{% endhighlight %}

A project is automatically created within that folder, along with the skeleton of the R package. You'll notice a folder named **R**, which is where you want to write and store all your script for the package. 