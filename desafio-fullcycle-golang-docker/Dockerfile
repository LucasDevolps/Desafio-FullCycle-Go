FROM golang:1.18

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build -o desafio-fullcycle-golang-docker

EXPOSE 8080

CMD ["./desafio-fullcycle-golang-docker"]
