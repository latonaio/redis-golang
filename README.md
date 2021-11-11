# redis-golang
redis-golang は、Golang で動作する(マイクロサービス)ランタイムにおける、Redis の適用方法を記載したレポジトリです。  
Golangの場合、ライブラリの依存関係を共通レポジトリで構築できないため、AIONでは、Golangランタイムにおける Redis の適用をマイクロサービス毎に定義しています。  
他方、AIONでは、Nodejsランタイム、Pythonランタイム で Redis を使用する場合、原則としてマイクロサービス毎に Redis を適用せずに、エッジコンピューティング環境毎に共通定義することとし、libraryとして共通化しております。詳細については、[redis-nodejs-client](https://github.com/latonaio/redis-nodejs-client)、[redis-python-client](https://github.com/latonaio/redis-python-client)を参照してください。

## 動作環境

* OS: Linux  
* CPU: ARM/AMD/Intel  
* Golang Runtime  

## Golang(マイクロサービス)ランタイム における Redis の適用方法  

Golang(マイクロサービスランタイム)環境で Redis を適用する場合は、go.modに以下のように記載します。  

```
module MODULE-NAME

go 1.17

require (
	github.com/go-redis/redis/v8 v8.11.4
	)
```