---
title: "Spd1.5 final blog post"
date: 2021-07-16T12:51:38-07:00
draft: false 
---

What is Snag a File?
Snag a file is a product in active development that allows users to make use of all of that bandwidth they pay for when downloading files or content off the internet

Why?
As someone who pays for expensive internet, I'd like to actually make use of what i'm paying for. Plus time is a resource and we often can be stuck downloading files for hours so I built Snag a file, a utility that makes use of Go’s concurrency features.

Challenges, I definitely had them since I was trying to build this application without using any packages or API's. I found myself learning about the Go language and its features. My first bug/issue was trying to figure out how to read the content of a URL and this is where I found myself initially learning there was a new request besides GET and POST it was called HEAD and it allowed me to get the byte size of a file, this was one of the largest portions of working with the data. Also when writing the algorithm that splits each set of bytes I had an overwrite bug that was causing 1 byte from the end of the last set to be duplicated into the next set. From here I was able to write these bytes to  .tmp files that were later written into a .js file.
As I continue working on this file downloader project I'd like to see if I can make this into a chrome extension that can visualize the progress of the download. 
