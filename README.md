# astparser

[![License MIT](https://img.shields.io/badge/License-MIT-blue.svg)](http://opensource.org/licenses/MIT) [![GoDoc](https://godoc.org/github.com/mkorolyov/astparser?status.svg)](http://godoc.org/github.com/mkorolyov/astparser) [![Go Report Card](https://goreportcard.com/badge/github.com/mkorolyov/astparser)](https://goreportcard.com/report/github.com/mkorolyov/astparser) [![Build Status](https://travis-ci.org/mkorolyov/astparser.svg?branch=master)](http://travis-ci.org/mkorolyov/astparser)


Simple golang structs ast parser

#### Get the package using:

```
$ go get -u -v github.com/mkorolyov/astparser
```

#### Usage

prepare loader config
```go
cfg := astparser.Config{
	InputDir:"somedir",
	//ExcludeRegexp "easyjson",
	IncludeRegexp:"event_",
}
```

Then you can load structs via

```go
files := astParser.Load(cfg)
```

`files` is a `map[string][]StructDef` where key is a file name and value is a list of structs defined in that file. 