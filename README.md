# A Simple nodeJS service - hello-nginxplus for docker and vm image

## Docker build

    docker build -t hello-nginxplus . no-cache

## Packer build
    packer build hello-gcp-image.json

## Usage

    docker run -p 8080:80 -p 8443:443 --rm -t hello-nginxplus

Test it with httpie

    http :3600/hello-nginxplus

Output would look like this
```
HTTP/1.1 200 OK
Connection: keep-alive
Content-Length: 472
Content-Type: application/json; charset=utf-8
Date: Sun, 02 Aug 2020 13:12:20 GMT
ETag: W/"1d8-rdUoVwbhNpQhCyfcbGHMxbV2njI"
X-Powered-By: Express

{
    "body": "",
    "connection": {},
    "fresh": false,
    "headers": {
        "accept": "*/*",
        "accept-encoding": "gzip, deflate",
        "connection": "keep-alive",
        "host": "localhost:3600",
        "user-agent": "HTTPie/2.2.0"
    },
    "hostname": "localhost",
    "ip": "::ffff:127.0.0.1",
    "ips": [],
    "method": "GET",
    "os": {
        "hostname": "XXXXX-iMac.local"
    },
    "path": "/hello-nginxplus",
    "protocol": "http",
    "query": {},
    "subdomains": [],
    "xhr": false
}
```
