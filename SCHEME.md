# streamblox

## Create ingest point

**<code>POST</code>** /ingest/new 

#### Body
```ruby
  {type: 'rtmp', token: 'your_token'}
```

#### Return
```ruby
{ingest_point: "rtmp://streamblox.host:1935/ingest-point-name", status: "success"}
```

#### Example
```shell
$ curl --data "type=rtmp&token=aBUjh123" http://streamblox.com/ingest/new
{ingest_point: "rtmp://streamblox.com:1935/aHUASb1231hs", status: "success"}
```

## Remove ingest point

**<code>DELETE</code>** /ingest/ingest-point-name

#### Return
```ruby
{status: "success"}
```

#### Example
```shell
$ curl -x DELETE http://streamblox.com/ingest/aHUASb1231hs
{status: "success"}
```

## List ingest points

**<code>GET</code>** /ingest

#### Return
```ruby
{status: "success", rtmp: ["ingest-point-name-a", "ingest-point-name-b"]}
```

#### Example
```shell
$ curl http://streamblox.com/ingest
{status: "success", rtmp: ["aHUAas12hs", "aHUASb1231hs"]}
```
