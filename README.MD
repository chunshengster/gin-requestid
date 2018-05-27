## Gin's Request ID Middleware

[Gin](https://github.com/gin-gonic/gin)'s Request ID middleware injects a request ID into the context for each request.

## Usage

```go
package main

import (
  "github.com/gin-gonic/gin"
  "github.com/thanhhh/gin-requestid"
)

func main() {
  r := gin.New() // without any middlewares

  r.Use(requestid.RequestID())

  r.Get("/", func() string {
    return "Hello world!"
  })

  r.Run(":8080")
}
```
