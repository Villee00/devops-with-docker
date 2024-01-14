FROM golang:1.19
EXPOSE 8080
WORKDIR /usr/src/app
COPY . .
RUN go build

CMD ["./server"]