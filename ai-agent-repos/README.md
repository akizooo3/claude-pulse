# ai-agent-repos

参照用に追加しているAIエージェント関連リポジトリ集（git submodule）。`git clone --recurse-submodules` もしくは

```bash
git submodule update --init --recursive
```

でソースは取得できますが、**そのまま動くのは agency-agents のみ**です。他はリポジトリごとに追加のインストール／登録作業が必要です。

| リポジトリ | clone後の状態 | 使うために必要なこと |
|---|---|---|
| [agency-agents](https://github.com/msitarzewski/agency-agents) | そのまま使える | エージェント定義（Markdown）集。Claude Code等に読み込ませるだけ |
| [Agent-Reach](https://github.com/Panniantong/Agent-Reach) | 別途インストール必須 | Python/CLIツール。AIエージェントに `docs/install.md` のURLを渡して自動インストールさせる方式。`pip install`・`mcporter`等の実行権限が前提（OpenClaw利用時は `tools.profile: coding` の設定が必要） |
| [OpenMontage](https://github.com/calesthio/OpenMontage) | 別途セットアップ必須 | Python 3.10+ / FFmpeg / Node.js 18+ が前提。`make setup`（またはvenv作成 → `pip install -r requirements.txt` → `npm install` → `.env`作成）を実行 |
| [codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp) | 別途インストール必須 | ネイティブバイナリ。`install.sh` / `install.ps1` でダウンロード・ビルドし、MCPクライアント（Claude Code等）への登録が必要 |
| [orca](https://github.com/stablyai/orca) | ソースをcloneしただけでは不可 | デスクトップアプリ本体。基本は公式配布のインストーラ（dmg/exe/AppImage）やHomebrew/AURで導入。ソースからのビルドは別途 `pnpm` ワークスペースが必要 |

各リポジトリの詳細な手順は、それぞれの README（`ai-agent-repos/<repo>/README.md`）を参照してください。
