### CHAPTER 10

# ”REST依存”の落とし穴

RESTの使用は、マイクロサービスにアクセスしてサービス間で通信するための最も一般的な選択です。
一般的なテンプレートフレームワーク（DropWizard、Spring Bootなど）のほとんどに、すでにサービステンプレートにRESTアクセスが組み込まれているほどです。
RESTがこのような一般的な選択肢であるのなら、なぜそれが落とし穴なのでしょうか？
”REST依存”の落とし穴とは、RESTを唯一の通信プロトコルとして使用し、マイクロサービスアーキテクチャを強化するメッセージングの可能性を考慮しないことです。
例えば、RESTfulなマイクロサービスアーキテクチャでは、どのように非同期通信を処理しますか？ブロードキャスト機能が必要ならどうでしょうか？
トランザクションの作業単位内で複数のリモートRESTful呼び出しを管理する必要がある場合はどうしますか？

マイクロサービスアーキテクチャにメッセージングを使用することを検討する際に注意すべき２つのタイプのメッセージング標準 — プラットフォーム固有の標準とプラットフォームに依存しない標準、があります。
プラットフォーム固有の標準には、Javaプラットフォーム用のJMSと.NETプラットフォーム用のMSMQがあります。
両方とも、使用しているメッセージング・プロバイダー（ベンダー）とは独立して、プラットフォーム内で使用される標準APIを記述しています。
例えば、Javaプラットフォームでは、APIを変更せずにブローカ（ActiveMQ、HornetQなど）を取り換えることができます。
APIは標準であり変化することはありませんが、これらは根本的にブローカ間で異なる独自のプロトコルです（これが、同じベンダーに対して同じクライアントJARとサーバーJARが必要な理由です）。
プラットフォーム標準のメッセージングプロトコルでは、使用している実際のベンダー製品や、使用されているワイヤレベルプロトコルよりも、共通のAPIを使用して移植性を重視しています。

現在のプラットフォームに依存しない標準はAMQPです。AMQPは、APIではなく、ワイヤレベルのプロトコルで標準化されています。
これにより、使用しているベンダー製品に関係なく、異なるプラットフォーム間で通信することができます。
例えば、RabbitMQを使用しているクライアントは、StormMQサーバと簡単に通信できます（同じプロトコルバージョンを使用しているとした場合）。
RabbitMQを使用しているAMQPは現在のところ、プラットフォームに依存しない性質のため、マイクロサービスアーキテクチャ内のメッセージングで最も一般的な選択肢です。
