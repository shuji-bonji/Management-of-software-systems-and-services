# ソフトウェア・システム・サービスに関わる管理

> ソフトウェア・システム・サービスの管理を **9つの視点** から包括的に整理したナレッジベース

| #   | 視点                                 | 中心的な問い                                  | 代表的フレームワーク        | ファイル                                                           | 状態     |
| --- | ------------------------------------ | --------------------------------------------- | --------------------------- | ------------------------------------------------------------------ | -------- |
| 1   | **プロジェクト**                     | どうやって作るか？                            | PMBOK, PRINCE2              | [project-process-map.md](./project-process-map.md)                 | 作成済み |
| 2   | **プロダクト**                       | 何を作り、どう育てるか？                      | Lean, Inspired (Cagan)      | [product-lifecycle-map.md](./product-lifecycle-map.md)             | 作成済み |
| 3   | **サービスマネジメント**             | どう安定的にサービスを届け続けるか？          | ITIL 4, ITSM                | [service-management-map.md](./service-management-map.md)           | 作成済み |
| 4   | **SRE / 信頼性エンジニアリング**     | どうシステムの信頼性を担保するか？            | Google SRE, SLI/SLO/SLA     | [sre-reliability-map.md](./sre-reliability-map.md)                 | 作成済み |
| 5   | **セキュリティ / コンプライアンス**  | どう安全を守り、法規制に準拠するか？          | ISMS (ISO27001), NIST, SOC2 | [security-compliance-map.md](./security-compliance-map.md)         | 作成済み |
| 6   | **データマネジメント**               | データをどう管理・活用・保護するか？          | DMBOK, データガバナンス     | [data-management-map.md](./data-management-map.md)                 | 作成済み |
| 7   | **プラットフォームエンジニアリング** | 開発者体験をどう最適化するか？                | Team Topologies, IDP        | [platform-engineering-map.md](./platform-engineering-map.md)       | 作成済み |
| 8   | **ポートフォリオ / プログラム**      | 複数プロダクト/プロジェクトをどう統括するか？ | SAFe, PfM, PgM              | [portfolio-program-map.md](./portfolio-program-map.md)             | 作成済み |
| 9   | **エンタープライズアーキテクチャ**   | 組織全体のIT構造をどう統制するか？            | TOGAF, Zachman              | [enterprise-architecture-map.md](./enterprise-architecture-map.md) | 作成済み |

## 9つの視点の関係性

```mermaid
graph TD
    EA["9. エンタープライズ<br>アーキテクチャ<br>組織全体のIT構造を統制"]
    PFM["8. ポートフォリオ /<br>プログラム<br>投資の最適配分"]

    PJ["1. プロジェクト<br>どう作るか"]
    PD["2. プロダクト<br>何を作り育てるか"]

    SM["3. サービス<br>マネジメント<br>安定的に届ける"]
    SRE["4. SRE<br>信頼性を担保"]

    SEC["5. セキュリティ /<br>コンプライアンス<br>安全を守る"]
    DM["6. データ<br>マネジメント<br>データを活用・保護"]
    PE["7. プラットフォーム<br>エンジニアリング<br>開発者体験を最適化"]

    EA -->|"方針・標準"| PFM
    PFM -->|"投資判断"| PJ
    PFM -->|"投資判断"| PD
    PJ -->|"成果物を移行"| SM
    PD -->|"サービスとして提供"| SM
    SRE -->|"信頼性を支える"| SM
    PE -->|"開発基盤を提供"| PJ
    PE -->|"開発基盤を提供"| PD
    SEC -->|"セキュリティ要件"| PJ
    SEC -->|"データ保護"| DM
    DM -->|"データ活用"| PD

    style EA fill:#2C3E50,color:#fff
    style PFM fill:#C0392B,color:#fff
    style PJ fill:#4A90D9,color:#fff
    style PD fill:#27AE60,color:#fff
    style SM fill:#2980B9,color:#fff
    style SRE fill:#E74C3C,color:#fff
    style SEC fill:#C0392B,color:#fff
    style DM fill:#F39C12,color:#fff
    style PE fill:#8E44AD,color:#fff
```

## 各ドキュメントの構成

各マップは以下の統一構造で記述されています：

- **全体フロー**（Mermaid図）— 工程の流れと関係性を一目で把握
- **他視点との比較** — この視点の特徴を明確にする対比表
- **工程ごとのセクション** — 各工程について以下を記述：
  - 目的
  - タスク一覧（テーブル形式）
  - リソース一覧（人・物・金のカテゴリ）
  - 成果物一覧（必須/任意の区分付き）
- **横断的な視点** — 他の8つの視点との連携ポイント
