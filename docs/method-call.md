# Method Call

Users can call a method like this:
```yoi
http client, send get request
  url: "http://localhost/me"
-> response (http response)
```

The above is the same as the following method call in `Java`:
```java
final HttpResponse response = httpClient.sendGetRequest("http://localhost/me");
```

## Method Call Chaining

Users can chain method calls like this:
```yoi
http client, send get request
  url: "http://localhost/me"
and parse name
-> name (string)
```

The above is the same as the following method call chaining in `Java`:
```java
final String name = httpClient
    .sendGetRequest("http://localhost/me")
    .parseName();
```

## Multiple Return Values

A method can return multiple values like this:
```yoi
user, give me your information
-> name (string)
-> email (string)
```
