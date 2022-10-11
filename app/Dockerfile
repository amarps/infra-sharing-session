from golang:alpine

RUN apk update && apk add --no-cache git

WORKDIR /app

COPY . .

RUN go mod tidy

run go build -o binary

EXPOSE 1234

ENTRYPOINT ["/app/binary"]