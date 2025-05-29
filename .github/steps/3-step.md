## ステップ3：ワークフローファイルにステップを追加する

_ワークフローにジョブを追加するなんて、素晴らしいですね！💃_

### 📖 理論：ジョブ内のステップ入門

[ステップ](https://docs.github.com/ja/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idsteps)はジョブの構成要素であり、コードのチェックアウト、コマンドの実行、オープンソースのアクションの使用などのタスクを自動化できます。ステップはジョブの環境内で順番に実行されますが、独立したプロセスとして実行されます。共有変数空間を持つ従来のコードとは異なり、[入力](https://docs.github.com/ja/actions/creating-actions/metadata-syntax-for-github-actions#inputs)と[出力](https://docs.github.com/ja/actions/creating-actions/metadata-syntax-for-github-actions#outputs-for-docker-container-and-javascript-actions)は明示的に宣言する必要があります。

> [!TIP]
> GitHub Actionsの最も優れた点は、コミュニティが既に多くの無料の便利なツールを構築している[マーケットプレイス](https://github.com/marketplace?type=actions)であり、それらを[見つけてカスタマイズ](https://docs.github.com/ja/actions/using-workflows/finding-and-customizing-actions)できます！

### ⌨️ アクティビティ：ワークフローファイルにステップを追加する

1. `welcome-workflow`ブランチで、`.github/workflows/welcome.yml`ファイルを開きます。

1. GitHub CLIを使用して新しいプルリクエストにコメントを投稿するために、`welcome`ジョブにステップを追加します。

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
       steps:
         - run: gh pr comment "$PR_URL" --body "Welcome to the repository!"
           env:
             GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
             PR_URL: ${{ github.event.pull_request.html_url }}
   ```

1. 変更を`welcome-workflow`ブランチに直接コミットします。

1. ステップ情報を追加すると、Monaがあなたの作業を確認し、この演習の次のステップを準備します！

<details>
<summary>問題が発生しましたか？ 🤷</summary><br/>

- `steps`セクションが`welcome`ジョブの下にあり、正しくインデントされていることを確認してください。
- 正しい環境変数が設定されていることを確認してください。

</details>