FROM golang:1.22-alpine AS builder

WORKDIR /usr/src/app/

COPY . ./

RUN go mod download

RUN go build -o product-catalog .

FROM alpine:latest

WORKDIR /app

COPY --from=builder /usr/src/app/product-catalog .

ENV PRODUCT_CATALOG_PORT=8080

ENTRYPOINT [ "./product-catalog" ]