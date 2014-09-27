# goamz - An Amazon Library for Go

[![Build Status](http://travis-ci.org/goamz/goamz.png?branch=master)](https://travis-ci.org/goamz/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services.

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/heatxsink/goamz/contributors)!

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/heatxsink/goamz/autoscaling
github.com/heatxsink/goamz/aws
github.com/heatxsink/goamz/cloudformation
github.com/heatxsink/goamz/cloudfront
github.com/heatxsink/goamz/cloudwatch
github.com/heatxsink/goamz/dynamodb
github.com/heatxsink/goamz/ec2
github.com/heatxsink/goamz/elb
github.com/heatxsink/goamz/iam
github.com/heatxsink/goamz/rds
github.com/heatxsink/goamz/route53
github.com/heatxsink/goamz/s3
github.com/heatxsink/goamz/sqs
github.com/heatxsink/goamz/sts

github.com/heatxsink/goamz/exp/mturk
github.com/heatxsink/goamz/exp/sdb
github.com/heatxsink/goamz/exp/sns
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/heatxsink/goamz](http://godoc.org/github.com/heatxsink/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/heatxsink/goamz/ec2`
* `$ go get github.com/heatxsink/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get github.com/motain/gocheck`

Then run go test as usual:

`$ go test github.com/heatxsink/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

$ gotest -i
