# env-manager

[![Build Status](https://img.shields.io/github/actions/workflow/status/user/env-manager/ci.yml?branch=main)]()
[![Go Version](https://img.shields.io/badge/go-1.22+-blue.svg)]()
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

Multi-environment variable manager with encryption and team sharing — designed for production workloads with a focus on reliability and developer ergonomics.

## Features

- Zero Dependencies: No external packages required for core functionality
- Structured Logging: Built-in structured logging with slog compatibility
- High Performance: Optimized for low-latency, high-throughput workloads

## Installation

```bash
go get github.com/user/env-manager@latest
```

## Quick Start

```go
package main

import (
	"fmt"
	"github.com/user/env-manager"
)

func main() {
	client := envmanager.New(
		envmanager.WithTimeout(30 * time.Second),
	)

	result, err := client.Run(context.Background())
	if err != nil {
		log.Fatal(err)
	}

	fmt.Println(result)
}
```

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
