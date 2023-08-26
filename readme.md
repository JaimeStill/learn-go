# Learn Go

Notes and results of working through the [Go Tutorials](https://golang.google.cn/doc/tutorial/)

Directory | Tutorial
---------|----------
[hello](./hello/) | [Getting started](https://go.dev/doc/tutorial/getting-started.html)
[modules](./modules/) | [Create a module](https://go.dev/doc/tutorial/create-module.html)
[database](./database) | [Accessing a relational database](https://go.dev/doc/tutorial/database-access)
[rest-api](./rest-api/) | [Developing a RESTful API with Go and Gin](https://go.dev/doc/tutorial/web-service-gin)
[generics](./generics/) | [Getting started with generics](https://go.dev/doc/tutorial/generics)
[fuzzing](./fuzzing/) | [Getting started with fuzzing](https://go.dev/doc/tutorial/fuzz)
[vulnerabilities](./vulnerabilities/) | [Find and fix vulnerable dependencies with govulncheck](https://go.dev/doc/tutorial/govulncheck)
[go-tour](./go-tour/) | [A Tour of Go](https://go.dev/tour/list)

## Debugging

To debug in VS Code, the [Delve](https://github.com/go-delve/delve) debugger needs to be installed:

```
go install github.com/go-delve/delve/cmd/dlv@latest
```