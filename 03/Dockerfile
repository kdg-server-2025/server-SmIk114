FROM golang:1.24 AS builder
WORKDIR /
COPY main.go .
RUN go build main.go

FROM alpine:3.22
WORKDIR /
COPY --from=builder main .
CMD ["./main"]