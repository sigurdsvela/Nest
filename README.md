# Nest - Swift Web Server Gateway Interface

[![Build Status](http://img.shields.io/travis/nestproject/Nest/master.svg?style=flat)](https://travis-ci.org/nestproject/Nest)

Nest provides a minimal interface between web servers supporting Swift and  web applications or frameworks. It’s designed to prevent tight coupling between web servers and web applications or frameworks. To enable the use of any framework or application with any server.

## Quick Links

- [Specification](Specification.md)

## Current Status

The specification is currently a draft, there are a couple of planned changes in the issue tracker and we welcome anyone to contribute to help improve the specification before we release version 1.0.0.

## Rationale and Goals

The primary goal of Nest is to enable the use of any framework or application with any server. To prevent tight coupling between web servers and web applications or frameworks.

Nest provides a minimal interface supporting every feature in HTTP. It must be extremely simple, and easy to implement for both servers and web applications.

The interface must not make use any external frameworks and only depend on core Swift language features.

## Example Application

A simple Hello World web application using the Nest interface:

```swift
func application(request:RequestType) -> ResponseType {
    return Response(.Ok, body: "Hello World")
}
```

## Testing

Along with providing a specification, Nest also provides a [test suite](https://github.com/nestproject/NestTestSuite) to ensure that a server correctly follows the specification, and to aid development of web servers.

## Implementations

### Web Servers

- [NestBox](https://github.com/nestproject/NestBox) - Basic Server Implementation.

## Web Frameworks

- [Turnstone](https://github.com/kylef/Turnstone) - URI Template Routing

### Other

- [Inquiline](https://github.com/nestproject/Inquiline) - A standard implementation of RequestType and ResponseType.
- [Padlock](https://github.com/nestproject/Padlock) - Nest middleware to lockup your web application.

## See Also

- [Python WSGI](https://www.python.org/dev/peps/pep-0333/)
- [Ruby Rack](http://rack.github.io)
- [Perl Web Server Gateway Interface](http://en.wikipedia.org/wiki/PSGI)

## License

Nest is licensed under the BSD license. See [LICENSE](LICENSE) for more information.

