FROM golang:1.16-alpine

WORKDIR /app

ENV PORT=8080
ENV REQUEST_ORIGIN=http://localhost:5000

COPY go.mod go.sum ./
RUN go mod download
COPY . .

RUN go build

EXPOSE 8080

CMD ["./server"]