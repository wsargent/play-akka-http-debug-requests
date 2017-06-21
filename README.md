# play-akka-http-debug-requests

Small project to see how to get Akka-HTTP server to spit out request and response.

Ideally we want something like [logRequest](http://doc.akka.io/docs/akka-http/current/scala/http/routing-dsl/directives/debugging-directives/logRequest.html) defined implicitly, so we can log all requests by turning up the configuration.  

But that doesn't seem to happen:

```
akka {
  loggers = ["akka.event.slf4j.Slf4jLogger"]
  loglevel = "DEBUG"
  logging-filter = "akka.event.slf4j.Slf4jLoggingFilter"
}

akka.http.server.log-unencrypted-network-bytes = on
```