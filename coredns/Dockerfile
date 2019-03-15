FROM golang:alpine

RUN apk update && apk add --no-cache git

WORKDIR /root
RUN git clone https://github.com/niktrix/coredns.git

WORKDIR  /root/coredns
RUN git checkout twentyfourbytes
RUN GOOS=linux GOARCH=amd64 go build -ldflags="-w -s" -o /go/bin/coredns

EXPOSE 53 53/udp

ENTRYPOINT ["/go/bin/coredns"]
CMD ["-conf", "/go/bin/Corefile"]
