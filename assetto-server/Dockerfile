FROM debian:bullseye-slim as builder

ARG VERSION

WORKDIR /var/lib/assetto-server
RUN apt update && apt install -y curl

RUN curl https://packages.microsoft.com/config/debian/11/packages-microsoft-prod.deb -L -o packages-microsoft-prod.deb && dpkg -i packages-microsoft-prod.deb && rm packages-microsoft-prod.deb
RUN apt update && apt install -y aspnetcore-runtime-6.0

RUN curl https://github.com/compujuckel/AssettoServer/releases/download/v$VERSION/assetto-server-linux-x64.tar.gz -L -o assetto-server-linux-x64.tar.gz
RUN tar -xf assetto-server-linux-x64.tar.gz && rm assetto-server-linux-x64.tar.gz && apt autoremove

ENTRYPOINT [ "/var/lib/assetto-server/AssettoServer" ]
