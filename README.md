# A Simple nodeJS service - hello-nginxplus for docker and vm image

## Docker build

    docker build -t mendhak/http-https-echo .

## Usage

    docker run -p 8080:80 -p 8443:443 --rm -t mendhak/http-https-echo

Then issue a request via your browser or curl -

    curl -k -X PUT -H "Arbitrary:Header" -d aaa=bbb https://localhost:8443/hello-world


