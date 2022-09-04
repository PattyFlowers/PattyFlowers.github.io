---
layout: post
title:  "Using Regular Expressions"
date:   2022-09-01
categories: Programming Learning
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---

str = "This, is. Split?"
str.split(/([?.,!])/)

would be
["This", ",", " is", ".", " Split", "?"]

Actually this is better, it removes the spaces also: str.split(/([?.,!])\s*/)