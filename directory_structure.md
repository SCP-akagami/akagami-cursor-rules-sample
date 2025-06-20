# ディレクトリ構造

## プロジェクトディレクトリ構成

```
akagami-cursor-rules-sample/
├── .git/                # Git管理用ディレクトリ
├── .github/             # GitHub設定・テンプレートディレクトリ
│   ├── ISSUE_TEMPLATE/  # Issueテンプレート格納ディレクトリ
│   │   ├── bug_report.yml       # バグ報告用テンプレート
│   │   ├── feature_request.yml  # 機能要求用テンプレート
│   │   ├── improvement.yml      # 改善提案用テンプレート
│   │   └── config.yml           # Issueテンプレート設定
│   └── pull_request_template.md # Pull Requestテンプレート
├── .cursor/             # Cursor AI用設定・ルール格納ディレクトリ
│   ├── rules/           # Cursorルールファイル（.mdc形式）
│   │   └── github_templates.mdc # GitHub テンプレート活用ルール
│   └── rules_background/# ルール背景・補足ドキュメント（.md形式）
└── directory_structure.md # 本ファイル（ディレクトリ構造説明）
```

## 各ディレクトリの役割と責務

### `.git/`
- **役割**: Gitによるバージョン管理用ディレクトリ
- **責務**: コミット履歴、ブランチ情報、設定等の管理
- **注意**: 通常、直接編集は行わない

### `.github/`
- **役割**: GitHub設定・テンプレート・ワークフローファイルを格納
- **責務**: GitHub上でのプロジェクト運用の標準化と自動化

#### `.github/ISSUE_TEMPLATE/`
- **役割**: GitHubのIssueテンプレート格納
- **責務**: 統一されたIssue作成のためのテンプレート管理
- **含有ファイル**:
  - `bug_report.yml` - バグ報告用構造化テンプレート
  - `feature_request.yml` - 新機能要求用構造化テンプレート
  - `improvement.yml` - 既存機能改善提案用構造化テンプレート
  - `config.yml` - Issueテンプレートの設定・カスタマイズ

#### `.github/pull_request_template.md`
- **役割**: Pull Requestテンプレート
- **責務**: 統一されたPR作成とレビュープロセスの標準化

### `.cursor/`
- **役割**: Cursor AI の設定・ルール・補助ドキュメントを格納
- **責務**: AI アシスタントの動作制御とプロジェクト固有のルール管理

#### `.cursor/rules/`
- **役割**: Cursor ルールファイル格納
- **責務**: AI の動作ルール定義（.mdc 形式）
- **含有ファイル**:
  - `project_onboarding.mdc` - プロジェクトオンボーディング手順
  - `docker_environment.mdc` - Docker環境関連ルール
  - `global.mdc` - グローバル設定・基本ルール
  - `cursorrules.mdc` - Cursor固有ルール
  - `commit_message.mdc` - コミットメッセージ生成ルール
  - `github_templates.mdc` - GitHubテンプレート活用ルール

#### `.cursor/rules_background/`
- **役割**: ルールの背景・補足説明用ドキュメント格納
- **責務**: ルールの詳細説明とコンテキスト提供（.md 形式）

## 設計パターン
- **現状**: プロジェクト初期段階のため、アプリケーション本体の構造は未確認
- **今後の方針**: アプリケーションコードや追加ディレクトリが作成された場合は、MVCパターンやレイヤードアーキテクチャ等の設計パターンを特定し、本ドキュメントを随時更新すること

## 更新履歴
- 初回作成: プロジェクトオンボーディング時の基本構造記録 