FROM debian:bullseye-slim as builder

ARG VERSION

WORKDIR /tmp
RUN apt update
RUN apt install -y curl
RUN curl https://github.com/pressly/goose/releases/download/v$VERSION/goose_linux_x86_64 -L -o /tmp/goose

FROM alpine:3.15

COPY --from=builder /tmp/goose /usr/bin/goose
RUN chmod +x /usr/bin/goose
