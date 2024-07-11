# Webcam Stream with HTTPS

Setting up a webcam stream using HTML, CSS, and JavaScript, and serving it over HTTPS using `http-server` and `mkcert`.

I served it through http on my macbook. http did not work on my phone, so I used https, and was able to stream on my phone too. 



## Setup Instructions

If you choose to use http, to run the server use this commannd python -m http.server 8000 (for python3)

If you choose to use https, follow these steps:

### 1. Install Node.js

### 2. Install `http-server`
sudo npm install -g http-server

### 3. Install mkcert

brew install mkcert
mkcert -install

### 4. Generate SSL certificates for your local server
mkcert localhost 192.168.1.11

This command will create two files: localhost+1.pem (the certificate) and localhost+1-key.pem (the key).

### 5. Run http-server with HTTPS
http-server -S -C localhost+1.pem -K localhost+1-key.pem -p 8000




