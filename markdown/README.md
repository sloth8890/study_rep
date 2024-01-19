# Introduction

This is markdown cheat sheet for those who need a remind markdown commands and learn tips of MARKDOWN.
# Help

Click Raw to see the script.
# Script

Use three backquotes mark and write language to create the script. 
```bash
python server.py
```
If you write programming language next to the first three backquotes, you can apply the corresponding theme. 
```python
import sys
print('hello world')
```
## Hyperlink

To create a hyperlink, employ square brackets and parentheses. Within the square brackets, specify the desired displayed text, and inside the parentheses, include the website link.
[This is the link](https://www.youtube.com)
[You can modify this](https://www.google.com.au/)

You can also link another markdown file by specified path from the current markdown.  
[Upper README file](../README.md)


# Checkbox List

**preview is only valid in github**

- [x] Checkbox 1
- [ ] Checkbox 2

# Table

| First header | Second header |

|a|b|c|
|:-|:-:|-:|
|left aligned|center aligned|right aligned|
|de|ee|fe|

# Image
![img](1.jpeg)


# Testing
From dlib github page, they are containing images in introduction of readme file.

[![GitHub Actions C++ Status](https://github.com/davisking/dlib/actions/workflows/build_cpp.yml/badge.svg)](https://github.com/davisking/dlib/actions/workflows/build_cpp.yml) [![GitHub Actions Python Status](https://github.com/davisking/dlib/actions/workflows/build_python.yml/badge.svg)](https://github.com/davisking/dlib/actions/workflows/build_python.yml)