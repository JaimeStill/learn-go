# Go Notes

## Module Setup

```powershell
mkdir greetings
cd .\greetings
go mod init example.com/greetings
cd ..

mkdir hello
cd .\hello
go mod init example.com/hello
cd ..
```

## Workspace Setup

```powershell
go work init .\greetings .\hello
```

## Setup Local Module Reference

In **hello.go**:

```go
package main

import (
    "fmt"

    "example.com/greetings"
)
```

Configure the local module reference:

```powershell
cd .\hello
go mod edit -replace example.com/greetings=../greetings
go mod tidy
```

## Build and Install

```powershell
# build the module
cd .\hello
go build

# discover the install path
go list -f '{{.Target}}' # $env:USERPROFILE\go\bin\hello.exe

# add to PATH
$env:PATH += ";$env:USERPROFILE\go\bin"

# install
go install

# verify hello.exe
cd ..
hello
```