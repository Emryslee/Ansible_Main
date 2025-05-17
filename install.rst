# Ansible環境セットアップ

## セットアップ手順
-------------------
1. pipenv のインストール:

      pip install pipenv

2. 仮想環境用Toolsインストールと仮想環境起動:

      pipenv install --dev
      pipenv shell

## Ansibleロールのセットアップ
-------------------
本リポジトリは、varsファイルと実行用スクリプトのみ存在しています。  
Ansibleのロールはすべてansible-galaxyを通じてRoles用リポジトリから取得されます。

## Rolesのインストール方法:

ロールレポジトリのDownloadはレポジトリdeploy時自動的に実施する仕組みとなります。
自動的にDowdloadされなかった場合下記コマンドを実行します。

      pipenv run ansible-galaxy install -r requirements.yml

## プレイブックの実行
------------------
Ansible プレイブックを実行するには以下のコマンドを使用してください。

      pipenv run ansible-playbook -i inventory.yml playbook.yml

実行前に `inventory.yml` および `playbook.yml` を環境に合わせて適切に編集してください。

## 注意事項
------------------
- ロールは外部リポジトリで管理されていることを前提としています。
- 実行前に、`./roles` ディレクトリ配下に必要なロールが揃っていることをご確認ください。