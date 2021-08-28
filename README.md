# HowToMakeAnEntireWebpageInPython
🐍 How to make an entire website in python
##  Why? 
This is a self-project, I wanted to learn how to make a full website in one python file! 

### Examples of use
#### Installing and running an entire site including content and hosting just by running one file

### Make a simple webpage
```
import os

#Create the files
fn = 'index.html'
content = """
<!DOCTYPE html>
<html lang="en">
<head>
<title>Adam's first website</title>
</head>
<body>
<h1>My name is Adam</h1>
<p>My favorite food is pizza</p>
<p>I like to play Fortnite</p>
</body>
</html>
"""
f = open(fn, 'w')
f.write(content)
f.close()
```
### Create and format CSS file
```
fn = 'main.css'
content = """
body {background-color: #000000;
      font-family: Arial}
h1, h2, p {color: #FFFFFF;
          margin: 0}
"""
f = open(fn, 'w')
f.write(content)
f.close()
```
### Create and format JavaScript file
```
fn = 'main.js'
content = """
var onLoad = function () {
var myHeading = document.querySelector('h1');
myHeading.textContent = 'Hello world!';
};
"""
f = open(fn, 'w')
f.write(content)
f.close()
```
### Update index.html with JAVASCRIPT tags
```
f = open(fn, 'r')
o = f.read()
f.close()
o = o.replace('</head>', '\n<script src="main.js"></script>\n</head>')
f = open(fn, 'w')
f.write(o)
f.close()
```
### Move CSS file to the same folder as the HTML file
```
os.rename('main.css', 'index.html/main.css')
```
### Move JS file to the same folder as the HTML file
```
os.rename('main.js', 'index.html/main.js')
```

