# Developing a Simple Webserver
Name: RAHINI .A
ID: 23012479

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content = """
<html>
<head>
<title>Webservers</title>
</head>
<body>
<hl>Top Five Web Application Frameworks</hl>
<h2>1.Django</h2>
<h3>2.Mean stack</h3>
<h4>3.React</h4>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8)
        self.end_headers()
        self.wfile.write(content.encode())

server_address = (' ', 80)
httpd = HTTPserver(server_address, HelloHandler)
httpd.server_forever()
```
# OUTPUT:
![Alt text](webserver.jpg)
# RESULT:

The program is executed succesfully
