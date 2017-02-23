# Summary

* [序文](README.md)

## アンチパターン
* [1. データ駆動型移行アンチパターン](AntiPatterns/Data-DrivenMigration/README.md)
  * [膨大なデータ移行](AntiPatterns/Data-DrivenMigration/TooManyDataMigrations.md)
  * [機能を最初に、データは最後に](AntiPatterns/Data-DrivenMigration/FunctionalityFirstDataLast.md)  

* [2. タイムアウトアンチパターン](AntiPatterns/TheTimeout/README.md)
  * [タイムアウト値を使用する](AntiPatterns/TheTimeout/UsingTimeoutValues.md)
  * [サーキットブレーカーパターンを使用する](AntiPatterns/TheTimeout/UsingTheCircuitBreakerPattern.md)

* [3. ”共有するように言われました”アンチパターン](AntiPatterns/TheIWasTaughtToShare/README.md)
  * [膨大な依存関係](AntiPatterns/TheIWasTaughtToShare/TooManyDependencies.md)
  * [共有コードテクニック](AntiPatterns/TheIWasTaughtToShare/TechniquesForSharingCode.md)

* [4. リーチインレポートアンチパターン](AntiPatterns/Reach-inReporting/README.md)
  * [マイクロサービスのレポートに関する問題](AntiPatterns/Reach-inReporting/IssuesWithMicroservicesReporting.md)
  * [非同期イベントプッシュ](AntiPatterns/Reach-inReporting/AsynchronousEventPushing.md)

## 落とし穴
* [5.”砂のごとき細かい粒度”の落とし穴](Pitfalls/GrainsOfSand/README.md)
  * [サービスの範囲と機能の分析](Pitfalls/GrainsOfSand/AnalyzingServiceScopeAndFunction.md)
  * [データベーストランザクションの分析](Pitfalls/GrainsOfSand/AnalyzingDatabaseTransactions.md)
  * [サービス・コレオグラフィーの分析](Pitfalls/GrainsOfSand/AnalyzingServiceChoreography.md)

* [6.”理由なき開発者”の落とし穴](Pitfalls/DeveloperWithoutACause/README.md)
  * [誤った判断](Pitfalls/DeveloperWithoutACause/MakingTheWrongDecision.md)
  * [ビジネス上の推進要因の理解](Pitfalls/DeveloperWithoutACause/UnderstandingBusinessDrivers.md)

* [7.”バンドワゴンへの搭乗”の落とし穴](Pitfalls/JumpOnTheBandwagon/README.md)
  * [利点と欠点](Pitfalls/JumpOnTheBandwagon/AdvantagesAndDisadvantages.md)
  * [ビジネス要件への適合](Pitfalls/JumpOnTheBandwagon/MatchingBusinessNeeds.md)
  * [他のアーキテクチャパターン](Pitfalls/JumpOnTheBandwagon/OtherArchitecturePatterns.md)

* [8.”変わらない契約”の落とし穴](Pitfalls/TheStaticContract/README.md)
  * [契約の変更](Pitfalls/TheStaticContract/ChangingAContract.md)
  * [ヘッダー・バージョニング](Pitfalls/TheStaticContract/HeaderVersioning.md)  
  * [スキーマ・バージョニング](Pitfalls/TheStaticContract/SchemaVersioning.md)

* [9.”まだ着かないの？”の落とし穴](Pitfalls/AreWeThereYet/README.md)
  * [レイテンシを計測する](Pitfalls/AreWeThereYet/MeasuringLatency.md)
  * [プロトコルを比較する](Pitfalls/AreWeThereYet/ComparingProtocols.md)

* [10. Give It a Rest Pitfall](Pitfalls/GiveItARest/README.md)
  * [非同期リクエスト](Pitfalls/GiveItARest/AsynchronousRequests.md)
  * [ブロードキャスト機能](Pitfalls/GiveItARest/BroadcastCapabilities.md)
  * [トランザクション要求](Pitfalls/GiveItARest/TransactedRequests.md)

* [著者紹介](AboutTheAuhor.md)
