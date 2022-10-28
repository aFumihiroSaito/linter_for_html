# Linter for HTML

## Node.jsのインストール


### asdf を使う場合

Mac の場合を前提に記載


Homebrewを使い、インストール

```
$ brew install asdf
```

asdf.shを.zshrcに追加する

```
$ echo -e "\n. $(brew --prefix asdf)/libexec/asdf.sh" >> ${ZDOTDIR:-~}/.zshrc
```

nodejs プラグインを追加する

```
$ asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
```

nodejs をインストールする


```
$ asdf install
```


### 直接インストールの場合

下記公式サイトより、各種 OS のパッケージをインストールする

https://nodejs.org/ja/download/

## npmパッケージのインストール

```
$ npm ci
```

## VSCodeの設定

### Extensionsのインストール

Recommendedにある下記のリストをインストールする

* Code Spell Checker
* Prettier - Code formatter
* Stylelint

## 使い方

### VSCode

html, cssファイル編集後の保存時、自動で整形される

一部構文エラーはVSCode上では表示されない場合がある

### npxコマンド

cssファイルのチェック

https://stylelint.io/user-guide/usage/cli/

```
$ npx stylelint "**/*.css"
```

htmlファイルの整形

https://prettier.io/docs/en/cli.html

```
$ npx prettier --write [filepath]
```

