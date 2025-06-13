# akagami-cursor-rules-sample

（このREADMEはCursorが作成しました）

## 概要

このプロジェクトは、Cursor AI の設定とルール管理に特化したサンプルプロジェクトです。
AI アシスタントの動作制御とプロジェクト固有のルール管理を効率的に行うためのベストプラクティスを提供します。

## 特徴

- **段階的作業プロセス**: 複数作業項目における段階的実行プロセスの実装
- **日本語対応**: 日本語での開発コミュニケーションに最適化
- **Docker環境対応**: Docker環境での開発作業に適した設定
- **品質管理**: 自動コミットメッセージ生成と品質チェック機能

## ディレクトリ構造

```
akagami-cursor-rules-sample/
├── .git/                    # Git管理用ディレクトリ
├── .cursor/                 # Cursor AI用設定・ルール格納ディレクトリ
│   ├── rules/              # Cursorルールファイル（.mdc形式）
│   │   ├── project_onboarding.mdc    # プロジェクトオンボーディング手順
│   │   ├── docker_environment.mdc    # Docker環境関連ルール
│   │   ├── global.mdc                # グローバル設定・基本ルール
│   │   ├── cursorrules.mdc           # Cursor固有ルール
│   │   └── commit_message.mdc        # コミットメッセージ生成ルール
│   └── rules_background/   # ルール背景・補足ドキュメント（.md形式）
├── directory_structure.md  # ディレクトリ構造説明
├── README.md               # プロジェクト概要（本ファイル）
└── .gitignore             # Git除外設定
```


### Core Rules
- **global.mdc**: 基本的な作業プロセスと品質管理のルール
- **cursorrules.mdc**: Cursor AI特有の設定とルール

### Development Rules
- **docker_environment.mdc**: Docker環境での作業に関するルールと注意事項
- **project_onboarding.mdc**: 新規プロジェクト参加時のオンボーディング手順

### Utility Rules
- **commit_message.mdc**: 自動コミットメッセージ生成のルール

## 開発フロー

1. **タスク分析**: 指示内容の詳細分析と実行計画の策定
2. **段階的実行**: 各作業項目の順次実行と進捗報告
3. **品質確認**: 各ステップでの検証と問題対応
4. **最終報告**: 成果物の評価と結果報告

## 注意事項

- **UI/UXデザインの変更は事前承認が必要**
- **技術スタックのバージョン変更は承認が必要**
- **指示以上の機能実装は事前提案が必要**
- **不明点は作業開始前に必ず確認**

## 貢献

このプロジェクトへの貢献を歓迎します。以下の手順に従ってください：

1. このリポジトリをフォーク
2. 機能ブランチを作成 (`git checkout -b feature/new-feature`)
3. 変更をコミット (`git commit -am 'Add new feature'`)
4. ブランチにプッシュ (`git push origin feature/new-feature`)
5. プルリクエストを作成

## ライセンス

このプロジェクトのライセンス情報は、プロジェクトの要件に応じて設定してください。

## 更新履歴

- 初回作成: プロジェクトオンボーディング時の基本構造記録
- README.md追加: プロジェクト概要と使用方法の文書化 