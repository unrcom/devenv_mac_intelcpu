# devenv_mac_intelcpu

Intel chip の macOS PC に、Webフロントエンドの開発に必要なツールをインストールする手順です

## Over view

- iTerm2
- VSCode
- Chrome
- Docker Desktop
- Git
- 

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

- https://iterm2.com　 の　[Download]　で iTerm.app がダウンロードできるので アプリケーションフォルダへ

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

- [管理]（歯車）マーク > 設定 > save で検索
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

## Chrome

インストールされていない場合はインストールしてください

- 公式サイトから googlechrome.dmg (Mac OS 版 Chrome DMG ユニバーサル インストーラ（x86、ARM)) をダウンロード
- googlechrome.dmg をダブルクリック
- Applications フォルダへ drag and drop
- Launchpad から起動する

### Webフロントエンドの開発に必要な拡張機能をインストールする

以下の拡張機能が必要になるのでインストールされていない場合はインストールしてください

- React Developer Tools
- Redux DevTools
- ModHeader

## Docker

- https://www.docker.com へアクセス
- まず右上の　Sign in　へ
- アカウントがない場合は Sign Up
- Sign in　済の状態で [Products] をホバー > [Docker Desktop] をクリックする
- [Mac with Intel Chip] をクリックする
- Docker.dmg ファイルをダブルクリック
- 「drog and drop」画面で Docker.dmg ファイルを Applications フォルダへ drop
- Launchpad Docker.app を起動する
  - 「Docker Desktop needs privileged access」のウィンドウが表示されたら [OK] をクリックしてヘルパーをインストールする
  - デスクトップの右上 Dockerアイコンがあるはずなのでこれをクリックして「Preferens...」を選択
  - 「General」の「Start Docker Desktop when you log in」にチェックが付いているか確認する (普段は起動したくないのであればこのチェックは外し、仕事前にチェックを入れてPCを再起動してください)
- Doker Desktop にログインする
  - デスクトップの右上 Dockerアイコンをクリックして「Dashboard」を選択
  - 起動したダッシュボードの右上で、自分の Docker id で　Sign in 済であることを確認する
  - Sign in　していなければ、あらためて Sign in する
  - Doker Desktop　(Dashboard) は閉じても問題ありません
- インストール確認

```
$ docker -v
```

## Git

- まず Git がインストールされているか確認しましょう

```
$ git --version
```

インストールされていない場合は以下を実施します

- Git は Homebrew でインストールするので、Homebrew　がインストールされているか確認してみましょう

```
$ brew -v
```

- インストールされていない場合は [公式ページ](https://brew.sh/index_ja) のインストールコマンドを実行する


```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- Git のインストールは以下のコマンドを実行する

```
$ brew install git
```

インストールが終わったらバージョンを確認してみてください

```
$ git --version
```

Git のインストール後はユーザ情報を登録します

- 現在のユーザ情報を確認するコマンド

```
$ git config --global -l
```

以下の３つの設定が確認できない場合は設定する

- user.name
- user.email
- core.quotepath

設定するコマンド (xxxx 部分は適当でいいですがメールアドレスが有効なものを指定してください)

```
$ git config --global user.name "xxxx"
$ git config --global user.email "xxxx@xxxx"
$ git config --global core.quotepath false
```

設定後は ``` git config --global -l ``` で設定を確認しておきましょう

end of md, thank you for your attention
