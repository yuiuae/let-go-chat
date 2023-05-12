let-go-chat
==========================================

> A let-go-chat written in Go and offers two methods for dealing with passwords


- Generates a hash for the password.
- Checks password by hash

## Installation

```bash
go get github.com/yuiuae/let-go-chat
```

## Usage

The following example generate hash for password.

```go
package main

import (
	"fmt"

	"github.com/yuiuae/let-go-chat"
)

var pass, hash string
var ch bool
var err error


func main() {
	// genereate hash
	pass = "PaSsWoRd"
	hash, err = hasher.HashPassword(pass)
	if err == nil {
		fmt.Printf("Hash = %s", hash)
	} else {
		fmt.Fprintf(os.Stderr, "HashPassword: %v\n", err)
		os.Exit(1)		
	}

	//check password
	ch = CheckPasswordHash(pass, hash)
	fmt.Printf("Password correct? - %t", ch)
	
}
```

# LICENSE
Serhii Khrystenko
