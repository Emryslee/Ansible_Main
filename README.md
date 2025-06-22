## システム要件

| 項目         | 内容                         | 備考                                                  |
|--------------|------------------------------|-------------------------------------------------------|
| Python       | 3.9以上                      | システムにPython3.9がインストールされていること      |
| pipenv       | 仮想環境構築・管理ツール     | pip install pipenv でインストール                    |
| Ansible      | 自動化構成管理ツール（仮想環境内） | Pipenvを使ってインストール（Pipfileに記述済み） |
| ansible-lint | AnsibleのLintツール          | Pipenvで開発環境用パッケージとしてインストール       |

## 主なリポジトリ構成
------------------
- `requirements.yml`: ロールレポジトリの定義ファイル
- `inventory.yml`: 対象ホストのインベントリファイル
- `playbook.yml`: メインplaybook
- `group_vars/` グループ単位の変数ファイル
- `host_vars/`: ホスト単位の変数ファイル
- `ansible.cfg`: ansibleの設定ファイル