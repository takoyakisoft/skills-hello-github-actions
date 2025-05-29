## ステップ5：マージして試してみる

_素晴らしいです！最初のGitHub Actionsワークフローを作成し、テストしました！_ 🚀

### 📖 理論：ワークフローが実行されるとき

ブランチでワークフローを作成すると、デフォルトブランチ（`main`）にマージされるまで、そのブランチでのみ有効になります。ワークフローがデフォルトブランチにある場合、リポジトリ全体に適用されます。

ブランチに関係なく、すべての新しいプルリクエストは、作成したワークフローを自動的にトリガーします。

> [!TIP]
> [workflow_dispatch](https://docs.github.com/ja/actions/using-workflows/events-that-trigger-workflows#workflow_dispatch)や[schedule](https://docs.github.com/ja/actions/using-workflows/events-that-trigger-workflows#schedule)のような一部のイベントトリガーは、ワークフローファイルがデフォルトブランチに存在する場合にのみ機能します。

### ⌨️ アクティビティ：プルリクエストをマージする

1. プルリクエストを`main`ブランチにマージします。

1. （任意）別のプルリクエストを開いて、ワークフローが再度実行されるのを確認してみてください！
