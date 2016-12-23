# serverless-janken

This application provides simple APIs to play Rock-paper-scissors game, using AWS serverless architecture.

## Requirement

* Serverless Framework v1.4

## Local mode

You can run serverless-janken in local environment using [serverless-offline](https://github.com/dherault/serverless-offline) and [serverless-dynamodb-local](https://github.com/99xt/serverless-dynamodb-local)

```
$ npm install
$ sls dynamodb install
$ sls dynamodb start

# Open new shell
$ sls offline

# Open new shell
$ curl 'http://localhost:3000/jankens?hand=rock&name=test' -X POST
{"player":"rock","computer":"scissors","unixtime":1482469235,"judge":"win"}
$ curl 'http://localhost:3000/jankens'
{"jankens":[{"unixtime":1482469235,"player_hand":"rock","judge":"win","player":"test","computer_hand":"scissors"},{"unixtime":1482418800,"player_hand":"rock","judge":"lose","player":"user1","computer_hand":"paper"}]}
```

## Deploy

```
$ sls deploy
$ curl '[endpoint]/jankens?hand=rock&name=test' -X POST
{"player":"rock","computer":"scissors","unixtime":1482469235,"judge":"win"}
$ curl '[endpoint]/jankens'
{"jankens":[{"unixtime":1482469235,"player_hand":"rock","judge":"win","player":"test","computer_hand":"scissors"},{"unixtime":1482418800,"player_hand":"rock","judge":"lose","player":"user1","computer_hand":"paper"}]}
```
