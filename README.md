# GitHub Actionsを使ってみよう

_GitHub Actionsのワークフローを作成して実行します。_

## ようこそ

自動化は、テスト、スキャン、レビュー、デプロイプロセスなどの反復的なタスクにとって重要であり、[GitHub Actions](https://docs.github.com/ja/actions)はそのワークフローを効率化するための最良の方法です。

- **対象者**: 開発者、DevOpsエンジニア、セキュリティエンジニア
- **学習内容**: GitHub Actionsワークフローの作成方法、実行方法、およびタスク自動化への活用方法。
- **作成するもの**: プルリクエスト作成時にコメントするActionsワークフロー。
- **前提条件**: [GitHub入門](https://github.com/skills/introduction-to-github)
- **所要時間**: この演習は30分未満で完了できます。

この演習では、次のことを行います：

1. ワークフローファイルを作成する
1. ジョブを追加する
1. 実行ステップを追加する
1. ワークフローの実行を確認する
1. プルリクエストをマージする

### この演習の始め方

演習を自分のアカウントにコピーし、お気に入りのOctocat（Mona）が最初のレッスンを準備するのに**約20秒**待ってから、**ページを更新してください**。

[![](https://img.shields.io/badge/Copy%20Exercise-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/new?template_owner=skills&template_name=hello-github-actions&owner=%40me&name=skills-hello-github-actions&description=演習:+GitHub+Actionsワークフローの作成と実行&visibility=public)

<details>
<summary>問題が発生しましたか？ 🤷</summary><br/>

演習をコピーする際は、以下の設定をお勧めします：

- 所有者には、リポジトリをホストする個人アカウントまたは組織を選択してください。

- プライベートリポジトリはActionsの実行時間を使用するため、パブリックリポジトリを作成することをお勧めします。

演習が20秒経っても準備できない場合は、[Actions](../../actions)タブを確認してください。

- ジョブが実行中かどうかを確認してください。単にもう少し時間がかかる場合があります。

- ページに失敗したジョブが表示される場合は、Issueを送信してください。素晴らしい、バグを見つけましたね！🐛

</details>

---

&copy; 2025 GitHub &bull; [行動規範](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MITライセンス](https://gh.io/mit)