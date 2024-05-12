# versioninfo [![GoDoc](https://godoc.org/github.com/grooverlabs/versioninfo?status.svg)](https://godoc.org/github.com/grooverlabs/versioninfo)

Fork of github.com/carlmjohnson/versioninfo

Importable package that parses `debug.ReadBuildInfo()` for inclusion in your Go application.

Requires Go 1.18+ for Git revision information, but compatible with prior versions of Go.

## Examples

```go
package main

import (
    "fmt"

    "github.com/grooverlabs/versioninfo"
)

func main() {
    fmt.Println("Version:", versioninfo.Version)
    fmt.Println("Revision:", versioninfo.Revision)
    fmt.Println("DirtyBuild:", versioninfo.DirtyBuild)
    fmt.Println("LastCommit:", versioninfo.LastCommit)
}
```

You may use the concatenated information provided by `versioninfo.Short()`:

```go
package main

import (
    "fmt"

    "github.com/grooverlabs/versioninfo"
)

func main() {
    fmt.Println("ShortInfo:", versioninfo.Short())
}
```

