---
layout: post
title:  "Ruby methods"
date:   2022-09-01
categories: Programming Learning Ruby
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
|`str.scan(regex or string)` -> Array with matches | Iterates through string looking for matches and returns array with the matches| `a = "Hello world".scan(/\w+/)` -> ["Hello", "world]      `"Hello world".scan(/\w+/) {|w| print w }` -> "Hello"  "world"| 

Formatting
`str.center(width, padstr = ' ') ⇒ String`| Centers string. If width is greater than the length of the string, it returns a new string of length width with our string centered and surrounded by padstr (otherwise it returns the string). If padstr is not given, it uses spaces.| `"cat".center(20)` -> "      cat        " `"space".center(20, '#')` -> "#######space#######"|

# Integer Methods

|Method| How it works | Examples |
|-----|------|-------|
|`Math.sqrt(value)` -> Float| It returns the square root of the given value as a float| `Math.sqrt(25)` -> 5.0 | 

# Array Methods

|Method| How it works | Examples |
|-----|------|-------|
|`[arr].each_with_index { |val,index| ... }` | For each element in the array, allows you to work with that element and its index| `a=[11,22,31,224,44].each_with_index { |val,index| puts "#{index} : #{val}" }` -> 0 : 11, 1 : 22...|
|`[arr].find { |element| condition? }` -> Element | Iterates through an array and returns the first match for which the condition evaluates true| `[1,2,3,4,5,6,7].find { |x| x.between?(2,4) }` -> 2|
|`[arr].select { |element| condition? }` -> New array| Iterates through the elements of the array, and returns a new array with the elements that evaluate true.| `[1,2,3,4,5].select { |x| x.odd? }` -> [1, 3, 5]|


# Hash Methods

|Method| How it works | Examples |
|-----|------|-------|
|`[hash].find { |key, value| condition? }` -> Element | Iterates through a hash and returns the first match for which the condition evaluates true| `{"a" => 1, "b" => 2, "c"=> 3}.find { |k, v| v.between?(2,3) }` -> {"b" => 2}|
|`[hash].select { |key, value| condition? }` -> {"key"=>value}| Iterates through a hash and returns a hash with all the key-value pairs that evaluate true to the condition.| `{a: 1, b: 2, c: 3}.select {|k, v| v < 2}` -> {a: 1}|


# Class Methods


# File methods
exist?()
File.open("students.csv", "r")
File.close  -> Very important to always close the files we have opened, or lots of bad things may happen!

Example of writing data into a file from our program:
```ruby
def save_students
  file = File.open("students.csv", "w") # We open (or create) our file "students.csv" with "write"("w") permission.
  @students.each do |student|           # We iterate over a pre-created array @students
    student_data = [student[:name], student[:cohort]]  # On every iteration we create a new array with the information
    csv_line = student_data.join(",") # We join our array together with commas as separator
    file.puts csv_line                # We insert out string into the file
  end 
  file.close                          # We close the file
end
```

Example of loading data from a file:
```ruby
def load_students
  file = File.open("students.csv", "r")  # We open a file "students.csv" with read permision.
  file.readlines.each do |line|          # We read each line and iterate
    name, cohort = line.chomp.split(',') # Paralel asignment - We split each line and assign the first value to name and the second to cohort.
    @students << {name: name, cohort: cohort.to_sym} # Shovel operator (<<), we introduce this values into the array @students.
  end
  file.close # We close our file. SUPER IMPORTANT!!!
end
```

Manually open and close a file.
```ruby
# Using new method
f = File.new("test.txt", "r") # reading
f = File.new("test.txt", "w") # writing
f = File.new("test.txt", "a") # appending

# Using open method
f = open("test.txt", "r")

# Remember to close files
f.close
# Automatically close a file using a block.
```
```ruby
f = File.open("test.txt", "r") do |f|
  # do something with file f
  puts f.read # for example, read it
end
```

# Command line methods
ARGV.first # first argument from the command line