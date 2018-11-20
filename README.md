# 事前作業
ワークショップを行うために必要な環境を準備します。

## 概要 / 説明
このPivotal Cloud Foundry ワークショップでは、Java アプリケーションを対象とした開発演習を行います。

演習を進める上で必要となるクライアント環境の準備を事前に行います。

## 前提 / 環境
クライアント環境は、MacOSまたはLinuxを推奨します。
以降の手順は、MacOSを前提として進めていますが、Linux / Windows の場合は適宜相当するツールの導入を行ってください。
(それぞれの手順は、今後掲載予定)


## 手順 / 解説
### Java SE Development Kit
下記サイトからプラットフォームに応じた JDK をダウンロードし、インストールを行います。
- [Java SE Development Kit 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

### cURL
下記サイトからプラットフォームに応じた cURL パッケージをダウンロードし、インストールを行います。
- [curl](https://curl.haxx.se/download.html)
  - [curl for Windows](https://curl.haxx.se/windows/)

- MacOS は標準で cURL が導入済みなのでインストール不要
- Windows で Git for Windows 同梱の利用も可能ですが、一部使用できないオプションがある事を注意してください。

#### PowerShell on Windows の場合
Windows では、curl は Invoke-WebRequest コマンドの別名としてエイリアス設定されています。
そのため、エイリアス設定を PowerShell 利用時のセッション中のみ無効化しておく必要があります。

```
PS C:> del alias:curl
```

### Cloud Foundry CLI
#### パッケージマネージャによるインストール
##### MacOS
```
$ brew tap cloudfoundry/tap
$ brew install cf-cli
```

##### Linux
```
$ wget -q -O - https://packages.cloudfoundry.org/debian/cli.cloudfoundry.org.key | sudo apt-key add -
$ echo "deb https://packages.cloudfoundry.org/debian stable main" | sudo tee /etc/apt/sources.list.d/cloudfoundry-cli.list
$ sudo apt-get update
$ sudo apt-get install cf-cli
```

```
$ sudo wget -O /etc/yum.repos.d/cloudfoundry-cli.repo https://packages.cloudfoundry.org/fedora/cloudfoundry-cli.repo
$ sudo yum install cf-cli
```
#### インストーラーによるインストール
- [Windows](https://cli.run.pivotal.io/stable?release=windows64&source=github)
- [MacOS](https://cli.run.pivotal.io/stable?release=windows64&source=github)
- [Linux-Debian/Ubuntu](https://cli.run.pivotal.io/stable?release=debian64&source=github)
- [Linux-RedHat/CentOS](https://cli.run.pivotal.io/stable?release=redhat64&source=github)

#### 導入確認
```
$ cf version
cf バージョン 6.40.1+85d04488a.2018-10-31
```

### Git
#### Gitクライアント
##### MacOS
```
$ brew install git
```

##### Linux
Debian/Ubuntu系の場合
```
$ sudo apt-get install git-all
```

RedHat/CentOS系の場合
```
$ sudo yum install git-all
```
#### GitHubアカウント
GitHub のアカウントを作成
- [GitHub サインアップ](https://github.com/join?source=experiment-header-dropdowns-home)

## まとめ / 振り返り
