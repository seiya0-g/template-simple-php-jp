# シンプルなPHP開発環境

シンプルなPHP開発環境のGitHubテンプレートリポジトリです。  
データベースを含めていない、PHPのみの開発環境です。  

## 動作環境

- `Windows` or `macOS`
- `Docker Desktop`

## 導入方法

ZIPをダウンロードするか、リポジトリを作成してクローンしてください。

- ZIPダウンロード
  - ソース コード アーカイブのダウンロード
    - <https://docs.github.com/ja/repositories/working-with-files/using-files/downloading-source-code-archives>
- リポジトリ作成
  - テンプレートからリポジトリを作成する
    - <https://docs.github.com/ja/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template>
  - リポジトリをクローンする
    - <https://docs.github.com/ja/repositories/creating-and-managing-repositories/cloning-a-repository>

## 環境構築

### docker-compose

- `docker-compose.yml`があるディレクトリで、`docker-compose up -d` コマンドを実行してください。

```bash
# ターミナルで実行
## ls コマンドで docker-compose.yml があるか確認
ls docker-compose.yml
## docker-compose で環境構築  ※ 時間がかかるので注意
docker-compose up -d
```

### 確認

以下のURLにアクセスし、PHP画面が表示されるか確認してください。

- <http://127.0.0.1:8080/index.php>

## 解説

### ドキュメントルート

ローカルの [html/](./html/) フォルダとコンテナ内のドキュメントルートのディレクトリの  
`/var/www/html` が同期しており、[html/](./html/) フォルダ内にPHPファイルを配置すると  
URLでアクセスできるようになります。  
