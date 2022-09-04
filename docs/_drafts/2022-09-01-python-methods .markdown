---
layout: post
title:  "Python methods"
date:   2022-09-01
categories: Programming Learning Python
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---

After working on Ruby problems for a while and doing some "pair programming", I realized my pairing pal had made a fantastic list of Ruby methods, categorised by object. I had been considering doing something similar for a while, to have an easily accessible source to find this information, and I think it is about time!. I will update the content as I learn the different methos. If you are programming in Python, you will want to have a look at the Python methods post instead.

Remember you can use `Ctrl + F` to find a particular method inside this post.

# String Methods

We will indicate the string that we want to apply the method to as "str".
When a method admits "!" at the end (e.g. str.gsub!), it means that instead of returning a new and modified string, it changes the string it is applied to permanently.

|Method| How it works | Examples| 
|-----|------|-------|
|`str.sub(pattern, replacement)` -> New string| We give it a pattern, character or word we want to substitute and the string we want to substitute it for. It only substitutes the first match and returns a new string. Admits "!".| `s.sub(/[aeiou]/, '*')`  -> "h*llo"|
|`str.gsub(pattern, replacement)` -> New string| It works like `.sub` but admits more than one substitution. Admits "!".| `s.gsub(/[aeiou]/, '*')` -> "h*ll*"|
|`str.chars` -> Array| Returns an array with each of the characters of a string as elements.| `"Hello".chars` -> ["H", "e", "l", "l", "o"]|
|`str.split(pattern)` -> Array| It divides a string with the desired pattern and returns an array with each of the divisions as elements| `"Hello".split("")` -> ["H", "e", "l", "l", "o"]   `"My name is Catonaut".split(" ")` -> ["My", "name", "is", "Catonaut"] `"Hey-you".split("-")` -> ["Hey", "you"]


# Integer Methods

|Method| How it works | Examples |
|-----|------|-------|
|`Math.sqrt(value)` -> Float| It returns the square root of the given value as a float| `Math.sqrt(25)` -> 5.0 | 

# Array Methods

|Method| How it works | Examples |
|-----|------|-------|
|`[11,22,31,224,44].each_with_index { |val,index| puts "index: #{index} for #{val}" if val < 30}`

# Hash Methods

|Method| How it works | Examples |
|-----|------|-------|
|

# Class Methods


