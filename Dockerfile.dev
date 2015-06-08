FROM golang

ENV GOPATH /go
COPY . /go/src/github.com/gliderlabs/registrator

WORKDIR /go/src/github.com/gliderlabs/registrator

RUN go get \
	&& go build -ldflags "-X main.Version dev" -o /bin/registrator

VOLUME /go/src/github.com/gliderlabs/registrator
CMD ["go get && go build -ldflags \"-X main.Version dev\" -o /bin/registrator && /bin/registrator"]