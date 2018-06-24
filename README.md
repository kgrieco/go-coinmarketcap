<h1 align="center">
  <br />
  <!--
  <img src="https://user-images.githubusercontent.com/168240/39501128-e66e2a18-4d6d-11e8-9e16-88655102da6c.png" alt="go-coinmarketcap" width="600" />
  -->
  <img src="https://user-images.githubusercontent.com/168240/41822669-34e92094-77a8-11e8-831e-67d38e686c21.png" alt="go-coinmarketcap" width="600" />
  <br />
  <br />
  <br />
</h1>

> The Unofficial [CoinMarketCap](https://coinmarketcap.com/) API client for [Go](https://golang.org/).

[![License](http://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/miguelmota/go-coinmarketcap/master/LICENSE.md) [![Build Status](https://travis-ci.org/miguelmota/go-coinmarketcap.svg?branch=master)](https://travis-ci.org/miguelmota/go-coinmarketcap) [![Go Report Card](https://goreportcard.com/badge/github.com/miguelmota/go-coinmarketcap?)](https://goreportcard.com/report/github.com/miguelmota/go-coinmarketcap) [![GoDoc](https://godoc.org/github.com/miguelmota/go-coinmarketcap?status.svg)](https://godoc.org/github.com/miguelmota/go-coinmarketcap)

Supports the CoinMarketCap Version [V2](https://coinmarketcap.com/api) and V1 Public API

## Documentation

[https://godoc.org/github.com/miguelmota/go-coinmarketcap](https://godoc.org/github.com/miguelmota/go-coinmarketcap)

## Install

```bash
go get -u github.com/miguelmota/go-coinmarketcap
```

## Getting started

```go
package main

import (
	"fmt"
	"log"

	cmc "github.com/miguelmota/go-coinmarketcap"
)

func main() {
	tickers, err := cmc.Tickers(&cmc.TickersOptions{
		Start:   0,
		Limit:   100,
		Convert: "USD",
	})
	if err != nil {
		log.Fatal(err)
	}

	for _, ticker := range tickers {
		fmt.Println(ticker.Symbol, ticker.Quotes["USD"].Price)
	}
}

```

## Examples

Check out the [`./example`](./example) directory and documentation.

## License

MIT
