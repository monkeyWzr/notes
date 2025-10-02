マトリクス情報をAWSに連携すれば実現できる。

## Sidekiq -> AWS ECS

Sidekiqプロセス側から直接実現する

定期ジョブ、もしくは:beatイベント。

感想: 高頻度で実行するのでSidekiqのリソースを食う。気持ち良くない。あとはログと実行履歴にノイズが残る

## Sidekiq -> Datadog Workflow -> AWS ECS

お金かかりそう。。

https://qiita.com/Bryant_Wang/items/01504bac9e1b18fed0f5
https://zenn.dev/mickeey/articles/bc07d7f906702b

## AWS Lambda -> AWS ECS

LambdaでSidekiqのRedisから必要な情報を取得してAWSに送る
