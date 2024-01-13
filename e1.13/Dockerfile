FROM golang:1.16

WORKDIR /usr/src/app

COPY . .

EXPOSE 8080

#RUN export PATH=$PATH:/usr/local/go/bin

RUN go build

RUN go test ./...

ENV REQUEST_ORIGIN=https://example.com

CMD ["./server"]

