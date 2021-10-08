# devenv_mac_intelcpu

React + Redux Toolkit + TypeScript　を用いた Webフロントエンドの開発環境を構築する手順です

## iTerm2

### iTerm2 がインストール済みか確認する

- りんご > このMacについて > 概要タブの [システムレポート]　をクリックする

「アプリケーション名」が「iTerm」のものがあればインストール済みです

### iTerm2 がインストール済みの場合

上記の システムレポート でバージョンがわかります

https://iterm2.com の Newsタブで最新リリースのバージョンがわかりますので、あまりにも古い場合はアップデートを検討してください

アップデート方法は　(おそらく) 

- iTerm2 (iTerm.app) を起動する
- iTerm2　> Check For Updates でアップデートできるんじゃないでしょうか

### iTerm2 がインストールされていない場合

- https://iterm2.com　の　[Download]　で iTerm.app がダウンロードできるので アプリケーションフォルダへ

## VSCode

### VSCode がインストール済みか確認する

- りんご > このMacについて > 概要タブの [システムレポート]　をクリックする

「アプリケーション名」が「Visual Studio Code」のものがあればインストール済みです

### VSCode がインストール済みの場合

上記の システムレポート でバージョンがわかります

https://code.visualstudio.com の Updatesタブで最新リリースのバージョンがわかりますので、あまりにも古い場合はアップデートを検討してください

- VSCode を起動する
- Code > 更新の確認 をクリックすると 更新をダウンロードしています と表示される　 (ダウンロード済であればこの手順はスキップ)
- ダウンロードが終わると Code > 再起動して更新　に表示が変わるのでこれを選択する
- VSCode　が再起動されるのであらためてバージョンを確認する

### VSCode がインストールされていない場合

- https://code.visualstudio.com の　[Download Mac Universal] で .app　がダウンロードできるので アプリケーションフォルダへ

### Webフロントエンドの開発に必要な拡張機能をインストールする

#### ES7 React/Redux/GraphQL/React-Native snippets

- [拡張機能]マーク > 「ES7」で検索
- インストールされていない場合はインストールする

#### Prettier - Code formatter

- [拡張機能] > 「prettier」で検索
- インストールされていない場合はインストールする

#### 環境設定を確認する

- [管理](歯車)マーク > 設定 > save で検索
- 「Editor: Format On Save」 にチェックが入っているか確認し、なければチェックする
- 右上の 「設定 (JSON) を開く」 のアイコンをクリックする
- 以下の設定が入っているか確認し、なければ追加する

```
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
```
  
  



