# parth

    go get "github.com/codemodus/parth"

Package parth provides functions for accessing path segments.

When returning an int of any size, the first whole number within the specified 
segment will be returned.  When returning a float of any size, the first 
decimal number within the specified segment will be returned.

## Usage

```go
func SegmentToASCII(path string, i int) (string, error)
func SegmentToBool(path string, i int) (bool, error)
func SegmentToFloat32(path string, i int) (float32, error)
func SegmentToFloat64(path string, i int) (float64, error)
func SegmentToInt(path string, i int) (int, error)
func SegmentToInt16(path string, i int) (int16, error)
func SegmentToInt32(path string, i int) (int32, error)
func SegmentToInt64(path string, i int) (int64, error)
func SegmentToInt8(path string, i int) (int8, error)
```

### Setup

```go
import (
    "fmt"

	"github.com/codemodus/parth"
)

func main() {
	path := "/zero/1"

    out0, err := parth.SegmentToASCII(path, 0)
	if err != nil {
		fmt.Println(err)
	}
	fmt.Println(out0)
	
	out1, err := parth.SegmentToInt(path, 1)
    if err != nil {
    	fmt.Println(err)
    }
   	fmt.Println(out1)
}
```

## Documentation

View the [GoDoc](http://godoc.org/github.com/codemodus/parth)
