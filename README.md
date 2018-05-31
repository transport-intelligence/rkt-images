# References

## Rkt containers
* http://github.com/rkt/rkt/blob/master/Documentation/getting-started-guide.md
* http://github.com/transport-intelligence/rkt-images

## Go programmation language

# Installation

## MacOS
```bash
$ brew install go
```

## Fedora
```bash
$ dnf -y install golang
```

# Build a Go application
## Build with the native Go compiler
```bash
$ CGO_ENABLED=0 go build -ldflags '-extldflags "-static"' app/go/hello.go
```

## Build with gccgo
```bash
$ go build -compiler gccgo -gccgoflags '-static' app/go/hello.go
```

## Execute and check
```bash
$ ./hello &
$ curl http://localhost:5000
2018/05/31 22:26:06 request from 127.0.0.1:61442
hello
$ kill %1
```


