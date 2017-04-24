---
layout: post
title: "Easier collaboration with R googlesheets package"
date: "2016-07-16"
tags:
 - R
 - collaboration
published: true
comments: true
---

`googlesheets` is a really useful package developed by [Jennifer Bryan](https://twitter.com/JennyBryan), enabling users to connect to and work with google sheets through R. That's pretty useful when you want to collaborate with others on the same document, among other things!

To get started:


```r
# Install Google Sheets library
devtools::install_github("jennybc/googlesheets")

# Attach it to the session
library(googlesheets)

# Authorize user
gs_auth(new_user = TRUE) ## To authorize your google account for use by googlesheets

# List google sheets in your drive
gs_ls()

# Read in spread-sheet using shareable link (from File -> Share)
bt = gs_url("https://your/sheet's/shareable/link")
bt

# Open spread sheet in browser
# gs_browse(bt) ## Opens sheet in browse

# Read in sheet of your interest
sh = gs_read(bt, ws = 2) # choosing sheet 2

# Convert to dataframe if you want/need
df = as.data.frame(sh)
str(df)
df

# And we're done!! Onwards to using this :) 
```
 
Github repo for package: https://github.com/jennybc/googlesheets

Slides:  [Slides](https://speakerdeck.com/jennybc/googlesheets-1) for an [rOpenSci Community Call in March 2016](https://github.com/ropensci/commcalls/issues/9)

