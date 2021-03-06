GitDriveへようこそ
=================================
GitDriveはiOSのために設計された、モバイル端末上で実行するGitバージョンコントロールソフトです。これによってお持ちのiOSデバイスがフル機能のGitバージョンコントロールサーバーとなる。AppStoreからダウンロードしてインストールするだけで、煩雑なセットアップが必要せず、1分以内でGitサーバーを構築することができます。Git Smart転送プロトコルを完全に再現し、転送は安定で高速、さらにレポジトリへのアクセス権限制御も提供しており、、レポジトリに対するshallow更新とダウンロード操作が可能となっています。

Gitの分散型アーキテクチャによって、単一のノードの破損はシステム全体のダウンに繋がりません。したかってGitDriveはGitストレージネットワークのノードとして適しています。さらに、このノードは可搬性があります。

GitDriveはフル機能のGitサーバーであるほかに、Gitクライアントの機能も提供します。App内で直接レポジトリを管理でき、ファイルを直接閲覧することもできます。

クラシックのコードマネジメントツールと違い、GitDriveはお持ちのソースコードをご自分のデバイスで保存することができます。さらにiCloudをご利用であれば、すべてのレポジトリが自動的にすべてのデバイスに同期されます。これによってiPhoneやiPadのストレージで大事なデータを保管することができます。小型の開発チームにとっても、便利にデータを交換することが可能になります。同時に、ご自身でGitサーバーを構築するような手間とコストがかかりません。

## クイック スタート
#### Gitチュートリアル
もしGit自身に対してまだよく分からないのであれば、こちらのGitチュートリアルをご参考ください。
[Gitチュートリアル](https://backlog.com/ja/git-tutorial/intro/intro1_1.html)

#### 既存のローカルレポジトリをGitDriveにアップロードする方法
- お使いの端末とPCが同じWiFiネットワークに接続していることを確認してください。
- GitDriveを起動し、Gitサーバーが実行していることを確認してください。スライドバーが青の状態は起動状態です。 ***（サイドメニュー --> サーバー状態）***。
- GitDrive Finderを起動し、FinderがGitDriveのためにローカルでドメイン名解決を行います。
- Git Griveで新しいレポジトリを作成します ***（サイドメニュー --> すべてのレポジトリ --> 新しいレポジトリ）***，***myrepo*** を入力して　***完了***　をクリックします。
- ローカルGitレポジトリに入った後に、以下のコマンドを入力してリモートGitレポジトリの追加を行います。

```
git remote add myrepo http://<IPアドレス>/myrepo
```
- 以下のコマンドを入力して、ローカルレポジトリをGitDriveにPushします。

```
git push myrepo refs/heads/*:refs/heads/*
```

#### GitDrive上のレポジトリをローカルにダウンロードする方法

- お使いの端末とPCが同じWiFiネットワークに接続していることを確認してください。
- GitDriveを起動し、Gitサーバーが実行していることを確認してください。スライドバーが青の状態は起動状態です。 ***（サイドメニュー --> サーバー状態）***。
- GitDrive Finderを起動し、FinderがGitDriveのためにローカルでドメイン名解決を行います。
- ローカルで以下のコマンドを入力して新しいレポジトリを作成します。

```
git clone http://<IPアドレス>/your_repo_name
```
- または、以下のコマンドを入力してshallowのレポジトリを作成します。

```
git clone —-depth=1 http://<IPアドレス>/your_repo_name
```

#### GitDrive Finder

端末が異なるネットワークに接続する場合があるため、ドメイン名でサーバーにアクセスすることをお勧めします。しかしこれは毎回接続するネットワークが変わった際にHostファイルを変更することになるため、我々はGitDrive Finderを開発しました(/Tutorial/finderフォルダは配下にあります)。このツールはJavaで開発されたため、ご利用するにはOSの制限がありません。

GitDrive Finderはネットワーク上のGitDriveを自動的に発見し、Hostファイルにドメイン名とIPアドレスの関連付けを追加します。セキュリティのため、この際は端末にアクセスするためのパスコードを求めることがあります。***（サイドメニュー --> IPアドレスの右側）***，端末のパスコード入力後、，***OK*** をクリックして検索を始めます。パスコードが一致する端末のみ発見されます。検索を開始する前にAppが起動していることを確認してください。

自動設定ツールはシステムのHostファイルを変更するため、Windowsにおいては管理者権限で実行する必要があります。同様に、Mac、Unix、またはLinuxにおいてはsudoで実行する必要があります。そうでなければHostファイルを変更することができません。

***サイドメニュー --> 設定 --> サーバー*** でサーバーのドメイン名を設定することができます。一度設定が完了すると、異なるネットワークに接続しても、再度Finderを実行することで自動的にお使いのドメイン名を最新のIPアドレスに更新できます。

目次
=================================
- [レポジトリ管理](./docs/chapter_1_ja.md)
- [レポジトリ内容閲覧](./docs/chapter_2_ja.md)
- [コミット履歴](./docs/chapter_3_ja.md)
- [Gitサーバー管理](./docs/chapter_4_ja.md)

