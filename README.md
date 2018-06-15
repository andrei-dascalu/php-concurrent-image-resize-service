# php-concurrent-image-resize-service

Example of concurrency in PHP using [Swoole](https://github.com/swoole/swoole-src).

## Requires
* Docker
* Docker compose

## Setup and run
* docker-compose up -d

## Restart service
* docker-compose restart app

## Watch logs
* docker-compose logs -f app

## Call
```
curl -X POST \
  http://127.0.0.1:8080/ \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 87334f0c-70cf-604c-ea3f-5aea3c6b1525' \
  -d '{
	"src": "https://url/to/image",
	"formats": [
		{"w": 100, "h": 50},
		{"w": 200, "h": 120, "q": 90}
	]
}'
```
