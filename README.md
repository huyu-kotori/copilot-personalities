# GitHub Copilot Personalities

GitHub Copilot に人格を与えるプロンプト集です。

# 使い方

自身のリポジトリにサブモジュールとして追加する方法をオススメします。

```bash
git submodule add https://github.com/numagotatu/copilot-personalities.git .github/personalities
```

そして、VSCode の設定としてこれを紐づけます。
`.vscode/settings.json`に以下のような内容を書き足してください。

```json
{
    "github.copilot.chat.codeGeneration.instructions": [
        {
            "file": ".github/personalities/kasukabe-tsumugi/personality.md" // ".github/personalities/{personal}/personality.md"
        },
        {
            "file": ".github/copilot-instructions.md" // あれば
        },
        {
            "file": ".clinerules" // あれば
        }
    ]
}
```