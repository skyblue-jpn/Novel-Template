<h1 align="center">Welcome to Novel-Template 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/skyblue-jpn/Novel-Template#readme" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/skyblue-jpn/Novel-Template/graphs/commit-activity" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/skyblue-jpn/Novel-Template/blob/master/LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/github/license/skyblue-jpn/Novel-Template" />
  </a>
</p>

### 🏠 [Homepage](https://github.com/skyblue-jpn/Novel-Template#readme)

This project is forked from [Novel-Template](https://github.com/haoblackj/Novel-Template/) by [haoblackj](https://github.com/haoblackj).

## Author

👤 **skyblue-jpn**

-   Github: [@skyblue-jpn](https://github.com/skyblue-jpn)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/haoblackj/Novel-Template/issues). You can also take a look at the [contributing guide](https://github.com/haoblackj/Novel-Template/blob/master/CONTRIBUTING.md).

## Show your support

Give a ⭐️ if this project helped you!

## 前提

-   説明に用いる環境は次のとおり。
    -   Visual Studio Code
        -   前提となる拡張機能は次のとおり。
            ```
            donjayamanne.githistory
            eamodio.gitlens
            EditorConfig.EditorConfig
            formulahendry.code-runner
            github.vscode-github-actions
            GitHub.vscode-pull-request-github
            haoblackj.convertwidth4novelwriter
            KnisterPeter.vscode-commitizen
            me-dutour-mathieu.vscode-github-actions
            mhutchie.git-graph
            pucelle.run-on-save
            redhat.vscode-yaml
            taichi.vscode-textlint
            TaiyoFujii.japanese-morpheme-handler
            TaiyoFujii.novel-writer
            ```
        -   VSCode の拡張機能メニューの「ワークスペースの推奨事項」から一括でインストールできる。
        -   無効化している拡張機能があった場合は、ワークスペース内で有効化しておく。

## テンプレートの使用方法

1.  テンプレートリポジトリページ中段の「Use this template」を押下する。
2.  作成したいリポジトリ名を入力する。
3.  公開リポジトリか非公開リポジトリかを選択する。
4.  Include all branches のチェックが空白になっていることを確認する。
5.  リポジトリ作成完了。

## リポジトリ作成後にやること

0.  リポジトリをローカルにクローン →VSCode で開く
1.  package.json 生成
    1.  VSCode でターミナルを開く。下記のコマンドが有用。
        > 特に変更していない限り、`Ctrl + @` で開けます。
    2.  ターミナルに以下のコマンドを投入して、package.json を修正する。
        ```bash:generate package.json
        yarn init
        ```
    3.  package.json が修正されたことを確認する。
        > 左ペインに表示されたファイルツリーで、`package.json`の右側に `M` と表示されたことを確認してください。
    4.  ターミナルに以下のコマンドを投入して、必要なパッケージをインストールする。
        ```bash:Install dependency
        yarn install
        ```
    5.  パッケージが正常にインストールされたことを確認する。
        > 左ペインに表示されたファイルツリーで、`yarn.lock`というファイルが新しく作成されていることを確認する。
    6.  上記で修正・作成されたファイルをコミット・プッシュする。
2.  個別ファイルを修正する。
    -   dict/dict.yml
        -   ミスタイプすることが多い固有名詞あたりを書いたらいいんじゃないですかね。
3.  これまで変更したファイルをコミット・プッシュする
    -   GitHub の認証情報を求めてきたら、都度サインインする。
    -   その他のエラーが出てきたら、都度ググる。
        -   初回構築の際によく生じるエラーについては、そのうち追記します。
4.  ターミナルに以下のコマンドを投入して、リポジトリの設定を実行する。
    ```bash:Configure Repository Setting
    ./configure_repository.sh
    ```

## 注意事項

-   原稿は `./Draft` ディレクトリに配置する。
-   原稿のファイル名は 3 桁の数字で始める。
    -   例: `001.md`, `002.md`, `003.md`, ...

## 自動校正とファイル変換

-   拡張機能 `run-on-save` が有効化されていると、ファイルを保存するたびに以下のコードが実行され自動校正が行われる。
    ```bash:Run on Save
    yarn run novel-proofread ${file} && sed -i '$ d' ${file}
    ```
-   拡張機能 `code-runner` が有効化されていると、実行ボタンを押すたびに以下のコードが実行されファイル変換が行われる。
    ```bash:Run on Save
    yarn run novel-build
    ```

## 📝 License

Copyright © 2023 [haoblackj](https://github.com/haoblackj).<br />
This project is [MIT](https://github.com/haoblackj/Novel-Template/blob/master/LICENSE) licensed.

---

_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
