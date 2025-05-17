# Ansibleプロジェクト

## システム要件
| 項目| 内容 | 備考 |
|:--------|:--------|:--------|
| Python | 3.9以上 | システムにPython3.9がインストールされていること |
| pipenv | 仮想環境構築・管理ツール | pip install pipenv でインストール |
| Ansible | 自動化構成管理ツール（仮想環境内） | Pipenvを使ってインストール(Pipfileに記述済み) |
| ansible-lint | AnsibleのLintツール | Pipenvで開発環境用パッケージとしてインストール |

## セットアップ手順
-------------------
1. pipenv のインストール:

      pip install pipenv

2. 仮想環境用Toolsインストールと仮想環境起動:

      pipenv install --dev
      pipenv shell

## Ansibleロールのセットアップ
-------------------
本リポジトリは、**varsファイル**と**実行用スクリプト**のみ存在しています。  
Ansibleのロールはすべて **ansible-galaxy** を通じてRoles用リポジトリから取得されます。

## Rolesのインストール方法:

ロールレポジトリのDownloadはレポジトリdeploy時自動的に実施する仕組みとなります。
自動的にDowdloadされなかった場合下記コマンドを実行します。

      pipenv run ansible-galaxy install -r requirements.yml -p ./roles

## プレイブックの実行
------------------
Ansible プレイブックを実行するには以下のコマンドを使用してください:

      pipenv run ansible-playbook -i inventory.yml playbook.yml

実行前に `inventory.yml` および `playbook.yml` を環境に合わせて適切に編集してください。

## 注意事項
------------------
- ロールは外部リポジトリで管理されていることを前提としています。
- 実行前に、`./roles` ディレクトリ配下に必要なロールが揃っていることをご確認ください。