FROM golang:1.8-alpine
#FROM golang:latest
ADD . /go/src/hello-app
RUN go install hello-app

FROM alpine
COPY --from=0 /go/bin/hello-app .
ENV PORT 8080
CMD ["./hello-app"]
