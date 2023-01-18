# Developing a Simple Webserver

# AIM:
PRAVIN RAJ.A 22007200

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
from http.server import HTTPServer, BaseHTTPRequestHandler

content ="""
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_adress =('',80)
httpd =HTTPServer(server_adress, HelloHandler)
httpd.serve_forever()
```


# OUTPUT:
# server side view:
![image](https://user-images.githubusercontent.com/118707879/211472439-07011d63-6e77-4159-96e8-13270220f2ef.png)

# client side view
![Screenshot_20230110_111335](https://user-images.githubusercontent.com/118707879/211472650-f17c7756-153f-4a50-b749-638edfe76142.png)


# RESULT:

The program is executed succesfully
