# Summary

* [序文](README.md)

## アンチパターン
* [1. データ駆動移行アンチパターン](AntiPatterns/Data-DrivenMigration/README.md)
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
* [5.「砂のごとき細かい粒度」の落とし穴](Pitfalls/GrainsOfSand/README.md)
  * [サービスの範囲と機能の分析](Pitfalls/GrainsOfSand/AnalyzingServiceScopeAndFunction.md)
  * [データベーストランザクションの分析](Pitfalls/GrainsOfSand/AnalyzingDatabaseTransactions.md)
  * [サービス・コレオグラフィーの分析](Pitfalls/GrainsOfSand/AnalyzingServiceChoreography.md)

* [6.「理由なき開発者」の落とし穴](Pitfalls/DeveloperWithoutACause/README.md)
  * [誤った判断](Pitfalls/DeveloperWithoutACause/MakingTheWrongDecision.md)
  * [ビジネス上の推進要因の理解](Pitfalls/DeveloperWithoutACause/UnderstandingBusinessDrivers.md)

* [7.「バンドワゴンへの搭乗」の落とし穴](Pitfalls/JumpOnTheBandwagon/README.md)
  * [長所と短所](Pitfalls/JumpOnTheBandwagon/AdvantagesAndDisadvantages.md)
  * [ビジネスニーズとの一致](Pitfalls/JumpOnTheBandwagon/MatchingBusinessNeeds.md)
  * [他のアーキテクチャパターン](Pitfalls/JumpOnTheBandwagon/OtherArchitecturePatterns.md)

* [8. The Static Contract Pitfall](Pitfalls/TheStaticContract/README.md)

* [9. Are We There Yet Pitfall](Pitfalls/AreWeThereYet/README.md)

* [10. Give It a Rest Pitfall](Pitfalls/GiveItAResult/README.md)