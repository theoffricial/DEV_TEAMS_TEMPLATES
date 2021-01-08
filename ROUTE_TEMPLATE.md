# ROUTE TEMPLATE

## REQUEST

```http
PATCH /api/endpoint HTTP/1.1
Host: www.bing.com
User-Agent: curl/7.54.0
Accept: */*

{ 
    blabla: string,
    ...
    ...
}
```

## REPONSE

### 200 OK - SUCCESS

* one of body properties null, undefined or invalid

```http
HTTP/1.1 200 OK
SOME-HEADER-NAME: SOME-VALUE
..
..
SOME-HEADER-NAME: SOME-VALUE


{ completed: boolean, message?: string, data?: unknown }
```

### 201 CREATED - SUCCESS

* one of body properties null, undefined or invalid

```http
HTTP/1.1 201 CREATED
SOME-HEADER-NAME: SOME-VALUE
..
..
SOME-HEADER-NAME: SOME-VALUE


{ completed: boolean, message?: string, data?: unknown }
```

### 400 BAD_REQUEST - ERROR

* one of body properties null, undefined or invalid

```http
HTTP/1.1 400 BAD REQUEST
SOME-HEADER-NAME: SOME-VALUE
..
..
SOME-HEADER-NAME: SOME-VALUE


{ completed: boolean, message?: string }
```

### 403 FORBIDDEN - ERROR

* The requestor has no permissions to update class

```http
HTTP/1.1 403 FORBIDDEN
SOME-HEADER-NAME: SOME-VALUE
..
..
SOME-HEADER-NAME: SOME-VALUE


{ completed: boolean, message?: string }
```

### 404 NOT FOUND - ERROR

```http
HTTP/1.1 404 NOT FOUND
SOME-HEADER-NAME: SOME-VALUE
..
..
SOME-HEADER-NAME: SOME-VALUE


{ completed: boolean, message?: string }
```

### 500 INTERNAL SERVER ERROR - ERROR

* otherwise

```http
HTTP/1.1 500 INTERNAL SERVER ERROR
SOME-HEADER-NAME: SOME-VALUE
..
..
SOME-HEADER-NAME: SOME-VALUE


{ completed: boolean, message?: string }
```

## HEADERS EXAMPLES

```http
some-token: 12h3213ui123de2
Date: Sun, 10 Oct 2010 23:26:07 GMT
Server: Ubuntu
Last-Modified: Sun, 26 Sep 2010 22:04:35 GMT
ETag: "45b6-834-491sds30dcc1182c0"
Accept-Ranges: bytes
Content-Length: 12
Connection: close
Content-Type: text/html
```
