## ステップ1：ワークフローファイルを作成する

### 📖 理論：ワークフロー入門

**ワークフロー**とは、リポジトリで定義する自動化されたプロセスです。ワークフローは、`.github/workflows`ディレクトリに保存されたYAMLファイルで記述されます。各ワークフローは、プルリクエストのオープン、コードのプッシュ、Issueの作成など、リポジトリで発生する特定の[イベント](https://docs.github.com/ja/actions/learn-github-actions/events-that-trigger-workflows)によってトリガーされます。

ワークフローを使用すると、コードのビルド、テスト、デプロイなどのタスクを自動化でき、プロジェクト内のほぼすべてのアクティビティに応答できます。

> [!NOTE]
> さらに詳しく知りたい場合は、以下のリソースを確認してください：
> - [GitHub Actionsを理解する](https://docs.github.com/ja/actions/learn-github-actions/understanding-github-actions)
> - [ワークフローをトリガーするイベント](https://docs.github.com/ja/actions/learn-github-actions/events-that-trigger-workflows)

### ⌨️ アクティビティ：ワークフローファイルを作成する

1. このリポジトリを新しいブラウザタブで開き、こちらのタブで指示を読みながら作業できるようにします。

1. リポジトリの**Code**タブで、`welcome-workflow`という名前の新しいブランチを作成します。

   <img width="400" alt="ブランチ作成のスクリーンショット" src="https://github.com/user-attachments/assets/8aa4a918-c877-4214-9efe-c9a99ca6421b" />

1. `welcome-workflow`ブランチで、`.github/workflows`ディレクトリに移動します。

1. `.github/workflows`ディレクトリに、以下の内容で`welcome.yml`という名前の新しいファイルを作成します。

   ```yaml
   name: Post welcome comment
   on:
     pull_request:
       types: [opened]
   permissions:
     pull-requests: write
   ```

   > [!NOTE]
   > これは未完成のワークフローファイルです。エラーメッセージが表示されても正常です。一歩ずつ進めましょう！😎

1. 変更を`welcome-workflow`ブランチに直接コミットします。

1. ワークフローファイルをコミットすると、Monaがあなたの作業を確認し、この演習の次のステップを準備します！

<details>
<summary>問題が発生しましたか？ 🤷</summary><br/>

- ワークフローファイルを作成する際には、`welcome-workflow`ブランチにいることを確認してください。
- ファイルパスとYAMLのインデントを再確認してください。

</details>