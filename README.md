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
$ # Open new shell
$ sls offline
```

## Deploy

```
$ sls deploy
```
