## ステップ2：ワークフローファイルにジョブを追加する

素晴らしい出来です！🎉 ワークフローファイルを追加しましたね！

### 📖 理論：ジョブ入門

[ジョブ](https://docs.github.com/ja/actions/learn-github-actions/understanding-github-actions#jobs)とは、ワークフロー内で同じ[ランナー](https://docs.github.com/ja/actions/using-github-hosted-runners/about-github-hosted-runners)上でまとめて実行される一連のステップのグループです。各ジョブは`jobs`セクションで定義され、デフォルトでは独立して並行に実行されます。

ジョブは、ワークフローをコードのビルド、テスト、デプロイなどの論理的な単位に整理するのに役立ちます。

> [!TIP]
> [マトリックス戦略を使用して、複数のバリエーションで実行するジョブを定義](https://docs.github.com/ja/actions/using-workflows/using-a-matrix-for-your-jobs)できます。

### ⌨️ アクティビティ：ワークフローファイルにジョブを追加する

1. `welcome-workflow`ブランチで、`.github/workflows/welcome.yml`ファイルを開きます。

1. ファイルを編集して`jobs`セクションと、最新のUbuntuオペレーティングシステムで実行される`welcome`という名前のジョブを1つ追加します。

   ```yaml
   name: Post welcome comment
   on:
     pull_request:
       types: [opened]
   permissions:
     pull-requests: write
   jobs:
     welcome:
       name: Post welcome comment
       runs-on: ubuntu-latest
   ```

1. 変更を`welcome-workflow`ブランチにコミットします。

1. ジョブ情報を追加すると、Monaがあなたの作業を確認し、この演習の次のステップを準備します！

<details>
<summary>問題が発生しましたか？ 🤷</summary><br/>

- `jobs`セクションがYAMLファイルで正しくインデントされていることを確認してください。
- 正しいファイルとブランチを編集していることを確認してください。

</details>