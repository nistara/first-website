---
layout: post
title: "Writing your own R package"
date: "2016-05-01"
tags:
 - R
comments: true
published: false
---
Under construction

I made this post for an introduction to building and documenting your own R packages for the Davis R-users' group. It'll get you started on making basic R packages, and once you get the flavor of what it's all about, you can unleash your inner R genie to create your own tools! 

![]({{ nistara.github.io }}/_assets/images/2016-05-01-R-packages-post/2016-05-01-R-genie.png)

<br><br>
The tools you're going to need for this are:

- Git and github - [Karl Broman](http://kbroman.org/github_tutorial/pages/first_time.html) has great, succinct instructions for getting started with both

- R packages
    * **devtools** - facilitates the creation, publishing, and installation of your package
    * **roxygen2** - to easily document your packaage contents

<br>

## **Let's get started**

Once you''ve installed the libraries, create your package in the directory you want it to be placed:


{% highlight r %}
install.packages("devtools")
library("devtools")
devtools::install_github("klutometis/roxygen")
library(roxygen2)

Step
install.packages(c("devtools", "
devtools::create("package_path/demo")
{% endhighlight %}

A project is automatically created within that folder, along with the basic skeleton of an R package:


<img src="https://raw.githubusercontent.com/nistara/nistara.github.io/master/_assets/images/2016-05-01-R-packages-post/2016-05-01-new-package.png" width="250" height="175" />


<br>

 Now open the **.Rproj** file to start working on your package. You'll see something like the image below. The **R** folder is where you'll write and store all your R script.

   ![]({{ nistara.github.io }}/_assets/images/2016-05-01-R-packages-post/2016-05-01-1-start-screenI.png)



To enable version control using git and github, and subsequently host your package on github, change your project settings via **Tools** from the menu bar. _If you don't intend to use git/github, skip the following steps:_

   ![]({{ nistara.github.io }}/_assets/images/2016-05-01-R-packages-post/2016-05-01-2-start-screenII.png)

From Git/SVN in the project options, choose git.

   ![]({{ nistara.github.io }}/_assets/images/2016-05-01-R-packages-post/2016-05-01-3-choose-git.png)


You'll see git options in your project window now:
   ![]({{ nistara.github.io }}/_assets/images/2016-05-01-R-packages-post/2016-05-01-5-now-git.png)


