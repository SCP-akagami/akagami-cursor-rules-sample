# Docker環境管理・エラー対応ルール背景

このルールは、Docker環境での開発作業において発生する環境問題やエラーへの適切な対応を確保するために策定されました。

## [1. ターミナルコマンド実行前に、まず`dc up -d`でDockerコンテナを起動する](mdc:docker_environment.mdc#1)

復習機能実装時、「そのコマンドの前に dc up -d、dc exec app bash を実行して」との指示があり、Docker環境では事前のコンテナ起動が必要であることが判明した。

## [2. Djangoサーバー操作時は`dc exec app bash`でコンテナ内にアクセスしてから実行する](mdc:docker_environment.mdc#2)

Djangoコマンド（migrate、runserver等）は必ずDockerコンテナ内で実行する必要があり、この手順の省略により動作しない問題が発生する。

## [3. ターミナルコマンド実行が拒否された場合、ユーザーに手動実行を依頼し実行すべきコマンドを明確に示す](mdc:docker_environment.mdc#3)

マイグレーション作成時にターミナルコマンドが実行できず、ユーザーに「python manage.py makemigrations ebbing_memo」の手動実行を依頼した事例がある。

## [4. 権限エラーや環境問題が発生した場合、代替手順を提案し問題の原因を説明する](mdc:docker_environment.mdc#4)

権限エラーやパッケージ不足等の環境問題時は、単にエラーを報告するだけでなく、具体的な解決策を提示する。

## [5. モデル変更時はマイグレーション作成・適用の確認を行う](mdc:docker_environment.mdc#5)

`enable_revision`フィールド追加時、マイグレーションの作成と適用を確認することで、データベースとの整合性を保った。

## [6. テンプレート変更時はサーバー再起動の必要性を伝える](mdc:docker_environment.mdc#6)

トグルスイッチが表示されない問題が発生した際、Djangoサーバーの再起動により解決した。静的ファイルやテンプレートの変更時は再起動が必要。

## [7-10. 動作確認・エラー対応](mdc:docker_environment.mdc#7)

新機能実装後の動作確認手順を明確にし、問題発生時は段階的な原因切り分けとログ分析を行うことで、効率的な問題解決を実現する。 