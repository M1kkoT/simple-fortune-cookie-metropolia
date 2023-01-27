FROM golang:latest

USER root

RUN apt-get update

WORKDIR /app

COPY go.mod ./

RUN go mod download

COPY . ./

COPY ./static ./

RUN go build

EXPOSE 8080 

CMD ["go", "run", "frontend"]
