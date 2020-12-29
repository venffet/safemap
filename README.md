# safemap
The `map` type in Go support concurrent reads and writes. 

## usage

Import the package:

```go
import (
	"github.com/venffet/safemap"
)

```

```bash
go get "github.com/venffet/safemap"
```

The package is now imported under the "safemap" namespace.

## example

```go

    // Create a new map.
    m := safemap.NewSafeMap()

    // Stores item within map, sets "bar" under key "foo"
    m.Set("foo", "bar")

    // Retrieve item from map.
    if tmp := m.Get("foo"); tmp != nil {
        bar := tmp.(string)
        fmt.Println(bar)
    }  

    // Deletes item under key "foo"
    m.Delete("foo")
```
