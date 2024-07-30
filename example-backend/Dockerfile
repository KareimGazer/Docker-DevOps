FROM golang:1.16

WORKDIR /go/src/app

EXPOSE 8080

ENV REQUEST_ORIGIN=http://localhost:5000

COPY go.mod go.sum .

RUN go mod download

COPY . .

RUN go build

RUN chmod +x ./server

RUN go test ./...

CMD ["./server"]



