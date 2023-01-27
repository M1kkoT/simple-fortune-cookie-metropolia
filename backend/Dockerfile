FROM golang:latest

USER root
RUN apt-get update

WORKDIR /app

COPY go.mod ./
COPY go.sum ./

RUN go mod download

COPY *.go ./

RUN go build

EXPOSE 9000

CMD ["go", "run", "backend"]




