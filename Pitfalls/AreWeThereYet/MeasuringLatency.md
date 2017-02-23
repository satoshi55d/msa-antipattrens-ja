## レイテンシを計測する

本番環境（または本番相当の環境）にて、負荷をかけた上体でリモート呼出しのレイテンシを測定することは、
アプリケーションのパフォーマンスプロファイルを理解する上で重要です。
例えば、ある業務リクエストのために、4つのマイクロサービスが動作する必要があるとしましょう。
リモートアクセスレイテンシが100ミリ秒であると仮定すると、
その業務リクエストはリモートアクセスレイテンシだけで500ミリ秒かかることになるでしょう。（最初のリクエストとサービス間の4回のリモート呼出し）
これは、実際の業務リクエスト処理のために1行もないソースコードが実行された0.5秒のリクエスト時間です。
ほとんどのアプリケーションは、単にそのようなレイテンシを許容することはできません。

この落とし穴を回避する方法は、単純に選択したリモートアクセスプロトコル（REST等）の平均レイテンシを測定して判断することだと考えるかもしれません。
しかしながら、その手法では使用している特定のリモートアクセスプロトコルの平均レイテンシという1つの情報しか得ることができません。
もう1つの手法は、Java Message Service（JMS）、AMQP（Advanced Message Queuing Protocol）、
およびMicrosoft Message Queue（MSMQ）等の他のリモートアクセスプロトコルを使用して相対的なレイテンシを調査することです。