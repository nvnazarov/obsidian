#prog-lang 

```
go mod init
go run .
go test [-v]
go mod tidy
go build
go install
go get
go work init
go work use
go work edit
go work sync
```

```go
make(map[int]string)

// structs
type Vertex struct {
	X int
	Y int
}

// struct literals
Vertex{1, 2}
Vertex{X: 2}
Vertex{}

// pointers
i := &Vertex{1, 2}
*i.X = 10

// arrays
var a [10]int = [10]int{2, 3}

// slices
var s []int = a[1:4]  // slice does not copy elements
s = make([]int, 0, 5)
s = append(s, 0)
len(s) cap(s)

// for ... range
for i, v := range s {

}

// map
var m = map[string]Vertex{
	"a": {1, 1},
	"b": {2, 2}
}
delete(m, "a")
elem, ok = m["c"]

// func
f := func(x, y float64) {
	return math.Sqrt(x*x + y*y)
}
```

```go
package main

import "fmt"

func adder() func(int) int {
	sum := 0
	return func(x int) int {
		sum += x
		return sum
	}
}

func main() {
	pos, neg := adder(), adder()
	for i := 0; i < 10; i++ {
		fmt.Println(
			pos(i),
			neg(-2*i),
		)
	}
}
```

- methods

```go
func (v Vertex) Abs() float64 {
	return math.Sqrt(v.X*v.X + v.Y*v.Y)
}
func (v *Vertex) ...
```

- interface

```go
type Abser interface {
	Abs() float64
}

var a interface{} = "Hello"
s := a.(string)

switch v := i.(type) {
	case int:
		...
	case float64:
		...
	default:
		...
}
```

- Goroutines

