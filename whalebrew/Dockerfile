# WIP: it will obviously not list externally downloaded images.
# TODO: think

FROM golang:1.7.5-alpine

RUN apk add --no-cache git && \
    go get github.com/bfirsh/whalebrew && \ 
    cd /go/src/github.com/bfirsh/whalebrew && \
    git checkout tags/0.0.3 -b stable && \ 
    go build -o /go/bin/whalebrew && \
    apk del git
ENTRYPOINT ["/go/bin/whalebrew"]

