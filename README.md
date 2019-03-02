### grpc-go
---
https://github.com/grpc/grpc-go

```
go get -u google.golang.org/grpc
grpc_GO_LOG_VERBOSITY_LEVEL=99 GRPC_GO_LOG_SERVERITY_LEVEL=info
```

```go
const PickFirstBalancerName = "pick_first"

const Version = "1.20.0-dev"

var DefaultBackoffConfig = BackoffConfig{
  MaxDelay: 120 * time.Second,
}

var EnableTracing bool

var (
  ErrClientConnClosing = status.Error(codes.Canceled, "grpc: the client connection is closing")
)

var ErrClientConnTimeout = errors.New("grpc: timed out when dialing")

var ErrServerStopped = errors.New("grpc: the server has been stopped")

func Code(err error) codes.Code

func ErrorDesc(err error) string

func Errorf(c codes.Code, format string, a ...interface{}) error

type Stream interface {
  Context() context.Context
  
  SendMsg(m interface{}) error
  
  RecvMsg(m interface{}) error
}
```

```
```

