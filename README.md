# Ansibleプロジェクト セットアップ手順
## システム要件
| 項目| 内容 | 備考 |
|:--------|:--------|:--------|
| Python | 3.9以上 | システムにPython3.9がインストールされていること |
| pipenv | 仮想環境構築・管理ツール | pip install pipenv でインストール |
| Ansible | 自動化構成管理ツール（仮想環境内） | Pipenvを使ってインストール（Pipfileに記述済み |
| ansible-lint | AnsibleのLintツール | Pipenvで開発環境用パッケージとしてインストール |

## 環境セットアップ手順
```bash
# ① Pipenv環境を構築
pipenv install --dev

# ② 仮想環境に入る
pipenv shell

# ③ Ansibleのバージョン確認
ansible --version
```

