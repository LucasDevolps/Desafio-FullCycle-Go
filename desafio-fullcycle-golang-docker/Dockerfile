FROM golang:1.18-alpine AS build

WORKDIR /app

COPY . .

RUN go mod download

RUN CGO_ENABLED=0 GOOS=linux go build -ldflags="-s -w" -o /goapp

FROM scratch

COPY --from=build /goapp /goapp

ENTRYPOINT ["/goapp"]
