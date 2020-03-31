FROM golang:1.14-alpine as build

WORKDIR /src/
COPY hello.go /src/
RUN GOOS=linux go build -o /bin/hello

FROM scratch
COPY --from=build /bin/hello /bin/hello
ENTRYPOINT ["/bin/hello"]
