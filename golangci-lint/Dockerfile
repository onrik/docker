ARG GO_VERSION

FROM golang:${GO_VERSION}

RUN go install github.com/golangci/golangci-lint/cmd/golangci-lint@v1.64 && go clean -cache && go clean -modcache
RUN apk add make
