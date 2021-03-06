<a href="https://echo.labstack.com"><img height="80" src="https://cdn.labstack.com/images/echo-logo.svg"></a>

[![Sourcegraph](https://sourcegraph.com/github.com/SaulDoesCode/echo/-/badge.svg?style=flat-square)](https://sourcegraph.com/github.com/SaulDoesCode/echo?badge)
[![GoDoc](http://img.shields.io/badge/go-documentation-blue.svg?style=flat-square)](http://godoc.org/github.com/SaulDoesCode/echo)
[![Go Report Card](https://goreportcard.com/badge/github.com/SaulDoesCode/echo?style=flat-square)](https://goreportcard.com/report/github.com/SaulDoesCode/echo)
[![Build Status](http://img.shields.io/travis/SaulDoesCode/echo.svg?style=flat-square)](https://travis-ci.org/SaulDoesCode/echo)
[![Codecov](https://img.shields.io/codecov/c/github/SaulDoesCode/echo.svg?style=flat-square)](https://codecov.io/gh/SaulDoesCode/echo) 
[![Join the chat at https://gitter.im/SaulDoesCode/echo](https://img.shields.io/badge/gitter-join%20chat-brightgreen.svg?style=flat-square)](https://gitter.im/SaulDoesCode/echo)
[![Forum](https://img.shields.io/badge/community-forum-00afd1.svg?style=flat-square)](https://forum.labstack.com)
[![Twitter](https://img.shields.io/badge/twitter-@labstack-55acee.svg?style=flat-square)](https://twitter.com/labstack)
[![License](http://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://raw.githubusercontent.com/SaulDoesCode/echo/master/LICENSE)

## Feature Overview

- Optimized HTTP router which smartly prioritize routes
- Build robust and scalable RESTful APIs
- Group APIs
- Extensible middleware framework
- Define middleware at root, group or route level
- Data binding for JSON, XML and form payload
- Handy functions to send variety of HTTP responses
- Centralized HTTP error handling
- Template rendering with any template engine
- Define your format for the logger
- Highly customizable
- Automatic TLS via Let’s Encrypt
- HTTP/2 support

## Benchmarks

Date: 2018/03/15<br>
Source: https://github.com/vishr/web-framework-benchmark<br>
Lower is better!

<img src="https://i.imgur.com/I32VdMJ.png">

## [Guide](https://echo.labstack.com/guide)

### Example

```go
package main

import (
	"net/http"

	"github.com/SaulDoesCode/echo"
	"github.com/SaulDoesCode/echo/middleware"
)

func main() {
	// Echo instance
	e := echo.New()

	// Middleware
	e.Use(middleware.Logger())
	e.Use(middleware.Recover())

	// Routes
	e.GET("/", hello)

	// Start server
	e.Logger.Fatal(e.Start(":1323"))
}

// Handler
func hello(c echo.Context) error {
	return c.String(http.StatusOK, "Hello, World!")
}
```

## Help

- [Forum](https://forum.labstack.com)
- [Chat](https://gitter.im/SaulDoesCode/echo)

## Contribute

**Use issues for everything**

- For a small change, just send a PR.
- For bigger changes open an issue for discussion before sending a PR.
- PR should have:
  - Test case
  - Documentation
  - Example (If it makes sense)
- You can also contribute by:
  - Reporting issues
  - Suggesting new features or enhancements
  - Improve/fix documentation

## Credits
- [Vishal Rana](https://github.com/vishr) - Author
- [Nitin Rana](https://github.com/nr17) - Consultant
- [Contributors](https://github.com/SaulDoesCode/echo/graphs/contributors)

## License

[MIT](https://github.com/SaulDoesCode/echo/blob/master/LICENSE)
