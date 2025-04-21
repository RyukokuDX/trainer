# GitHub 初心者向け練習レポジトリ

このレポジトリは、GitHubの基本的な使い方を学ぶための練習用です。段階的にGitHubの機能を理解し、実践的に学ぶことができます。

## GitHubとは？

GitHubは、ソフトウェア開発のためのプラットフォームです。主な特徴は以下の通りです：

- コードのバージョン管理（変更履歴の管理）
- チーム開発のサポート
- コードの共有と公開
- プロジェクト管理機能

## 始め方

1. Gitの初期設定を行う
   - Windows (PowerShell推奨):
     1. [Git for Windows](https://gitforwindows.org/)からインストーラーをダウンロード
     2. インストーラーを実行し、デフォルト設定のまま「Next」を押してインストール
     3. インストール完了後、スタートメニューから「Git GUI」を起動
     4. 「Edit」→「Options」を選択
     5. 以下の項目を設定：
        - User Name: あなたの名前
        - Email Address: あなたのメールアドレス
     6. 「Save」をクリックして設定を保存

   - WSL (Ubuntu):
     ```bash
     # Gitのインストール（未インストールの場合）
     sudo apt update
     sudo apt install git
     ```

   - macOS:
     ```bash
     # Gitのインストール（未インストールの場合）
     brew install git
     ```

2. GitHubアカウントを作成する
   - [GitHub](https://github.com)にアクセス
   - 「Sign up」ボタンをクリック
   - 必要な情報を入力してアカウントを作成

3. Cursorをインストールする
   - [Cursor公式サイト](https://cursor.sh)からダウンロード
   - インストーラーを実行
   - GitHubアカウントでログイン

4. リポジトリをクローンする
   - Cursorの「File」メニューから「Clone Repository」を選択
   - リポジトリのURLを入力：`git@github.com:RyukokuDX/trainer.git`
   - 保存先のフォルダを選択

5. 練習課題に取り組む

## 基本的な用語

- **リポジトリ（Repository）**: プロジェクトの保存場所
- **コミット（Commit）**: 変更内容を記録すること
- **ブランチ（Branch）**: 開発の枝分かれを作成すること
- **プルリクエスト（Pull Request）**: 変更内容を提案すること
- **マージ（Merge）**: 変更内容を統合すること

## 練習課題

### 1. 基本的な操作
1. このリポジトリをクローン（ダウンロード）する
   - Cursorの「File」メニューから「Clone Repository」を選択
   - リポジトリのURLを入力：`https://github.com/RyukokuDX/trainer.git`
   - 保存先のフォルダを選択

2. `{学籍番号}`フォルダを作成し、
その中に自己紹介文を書いた`introduction.md`を作成する
   - Cursorのエクスプローラーで右クリック→「New Folder」で`{学籍番号}`フォルダを作成
   - 同様に右クリック→「New File」で`introduction.md`を作成
   - 以下の内容を入力：
     ```markdown
     # 自己紹介
     
     ## 名前
     あなたの名前
     
     ## 趣味
     - 趣味1
     - 趣味2
     
     ## 好きなプログラミング言語
     言語名とその理由
     ```

3. 新しいブランチを作成する
   - Cursorの下部ステータスバーの「main」をクリック
   - 「Create new branch」を選択
   - ブランチ名を入力：`feature/{学籍番号}`

4. 変更をコミットする
   - Cursorの左サイドバーの「Source Control」アイコンをクリック
   - 変更したファイルの横の「+」をクリックしてステージング
   - コミットメッセージを入力：「自己紹介文を追加」
   - 「Commit」ボタンをクリック
   - コミットメッセージの例：
     ```
     feat: 自己紹介文を追加

     - 名前、趣味、好きなプログラミング言語の情報を追加
     - Markdown形式で整形
     ```

5. 変更をプッシュ（アップロード）する
   - 「Source Control」パネルの「...」メニューから「Push」を選択
   - 初回プッシュ時は、GitHubの認証情報の入力を求められる場合があります
   - プッシュが成功すると、GitHubのウェブサイトで変更が確認できます

> **注意**: mainブランチへのプッシュはできません。必ず`feature/{学籍番号}`ブランチで作業してください。

### 2. ブランチの操作
1. `practice/todo.md`ファイルを作成する
   - 以下の内容を入力：
     ```markdown
     # 今週の目標
     
     - [ ] 目標1
     - [ ] 目標2
     - [ ] 目標3
     ```

2. 変更をコミットしてプッシュする
   - コミットメッセージ：「Todoリストの追加」
   - プッシュして変更をリモートリポジトリに反映

3. プルリクエストを作成する
   - GitHubのウェブサイトで「Compare & pull request」ボタンをクリック
   - タイトル：「Todoリストの追加」
   - 説明：「今週の目標をTodoリストとして追加しました」
   - 「Create pull request」をクリック

4. プルリクエストのレビューを待つ
   - リポジトリ管理者がレビューを行います
   - レビューコメントに基づいて必要な修正を行ってください
   - 修正後、同じプルリクエストに追加のコミットをプッシュできます
   - 承認後、リポジトリ管理者がマージを行います

> **注意**: mainブランチへのマージはリポジトリ管理者のみが行えます。練習者はプルリクエストの作成と修正までを行ってください。

### 3. コラボレーション
1. イシューを作成する
   - GitHubのウェブサイトで「Issues」タブをクリック
   - 「New Issue」ボタンをクリック
   - タイトル：「自己紹介文のフォーマットを統一したい」
   - 説明：「全員の自己紹介文を同じフォーマットにしましょう」
   - ラベル：「enhancement」を選択
   - 「Submit new issue」をクリック

2. プルリクエストにレビューコメントを付ける
   - プルリクエストの「Files changed」タブを開く
   - コメントを付けたい行の「+」をクリック
   - コメントを入力：「自己紹介文にプログラミング経験年数を追加するとよいと思います」

3. 変更を提案する
   - イシューに関連するブランチを作成
   - 提案する変更を実装
   - プルリクエストを作成してレビューを依頼

## 注意事項

- 練習用のリポジトリなので、自由に試してみてください
- 間違えても大丈夫です。GitHubでは変更履歴が残るので、いつでも元に戻せます
- 質問や不明な点があれば、イシューで質問してください 

## Cursorの設定

### Markdown関連の設定

Cursorでは、Markdownファイルの編集をサポートするための設定がいくつかあります。

#### 1. プレビューの表示
- `Ctrl + Shift + V`（Windows/Linux）または`Cmd + Shift + V`（macOS）でプレビューを表示
- プレビューは右側に表示され、リアルタイムで更新されます

#### 2. 拡張機能のインストール
1. `Ctrl + Shift + X`（Windows/Linux）または`Cmd + Shift + X`（macOS）で拡張機能パネルを開く
2. 以下の拡張機能を検索してインストール：
   - `Markdown All in One`: Markdownの編集をサポート
   - `markdownlint`: Markdownの文法チェック
   - `Markdown Preview Enhanced`: 拡張されたプレビュー機能

#### 3. 設定のカスタマイズ
1. `Ctrl + ,`（Windows/Linux）または`Cmd + ,`（macOS）で設定を開く
2. 以下の設定を推奨：
   ```json
   {
     "markdown.preview.breaks": true,
     "markdown.preview.doubleClickToSwitchToEditor": false,
     "markdown.links.openLocation": "beside",
     "markdown.validate.enabled": true,
     "markdown.validate.fragmentLinks": true
   }
   ```

#### 4. ショートカットキー
- 見出しの追加: `Ctrl + Shift + 1`〜`6`（Windows/Linux）または`Cmd + Shift + 1`〜`6`（macOS）
- 太字: `Ctrl + B`（Windows/Linux）または`Cmd + B`（macOS）
- イタリック: `Ctrl + I`（Windows/Linux）または`Cmd + I`（macOS）
- リストの追加: `Ctrl + Shift + L`（Windows/Linux）または`Cmd + Shift + L`（macOS）

## GitHubの認証設定（ちょっと発展）

GitHubでは、セキュリティを確保するために公開鍵認証を使用することを推奨しています。以下の手順で設定を行ってください。

### 1. 公開鍵の生成と登録

#### Windows (PowerShell)
```powershell
# SSHキーの生成
ssh-keygen -t ed25519 -C "あなたのメールアドレス"

# 生成された公開鍵の表示
cat ~/.ssh/id_ed25519.pub

# 表示された公開鍵をGitHubに登録
# 1. GitHubの設定画面（Settings）を開く
# 2. 左サイドバーの「SSH and GPG keys」を選択
# 3. 「New SSH key」をクリック
# 4. タイトルを入力（例：My Windows PC）
# 5. 公開鍵を貼り付け
# 6. 「Add SSH key」をクリック
```

#### Windows (WSL)
```bash
# SSHキーの生成
ssh-keygen -t ed25519 -C "あなたのメールアドレス"

# 生成された公開鍵の表示
cat ~/.ssh/id_ed25519.pub

# 表示された公開鍵をGitHubに登録
# 1. GitHubの設定画面（Settings）を開く
# 2. 左サイドバーの「SSH and GPG keys」を選択
# 3. 「New SSH key」をクリック
# 4. タイトルを入力（例：My WSL）
# 5. 公開鍵を貼り付け
# 6. 「Add SSH key」をクリック
```

#### macOS
```bash
# SSHキーの生成
ssh-keygen -t ed25519 -C "あなたのメールアドレス"

# 生成された公開鍵の表示
cat ~/.ssh/id_ed25519.pub

# 表示された公開鍵をGitHubに登録
# 1. GitHubの設定画面（Settings）を開く
# 2. 左サイドバーの「SSH and GPG keys」を選択
# 3. 「New SSH key」をクリック
# 4. タイトルを入力（例：My Mac）
# 5. 公開鍵を貼り付け
# 6. 「Add SSH key」をクリック
```

### 2. 接続テスト

各OS共通で以下のコマンドを実行して接続をテストします：

```bash
ssh -T git@github.com
```

成功すると以下のメッセージが表示されます：
```
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

### 3. SSHの設定ファイル

複数のGitHubアカウントや、異なる環境からアクセスする場合は、SSHの設定ファイルを使用すると便利です。

#### Windows (PowerShell/WSL) / macOS
```bash
# 設定ファイルの作成
mkdir -p ~/.ssh
touch ~/.ssh/config

# 設定ファイルの編集
# 以下の内容を追加：

# GitHubのメインアカウント
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519
    IdentitiesOnly yes

# GitHubの別アカウント（必要な場合）
Host github-alt
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_alt
    IdentitiesOnly yes
```

設定後、以下のように使用できます：
```bash
# メインアカウントの場合
git clone git@github.com:RyukokuDX/trainer.git

# 別アカウントの場合
git clone git@github-alt:RyukokuDX/trainer.git
```

### 4. リポジトリのクローン方法

公開鍵認証を使用する場合は、HTTPSではなくSSHのURLを使用します：

```bash
git clone git@github.com:RyukokuDX/trainer.git
```

## 参考リンク

- [GitHub公式ドキュメント](https://docs.github.com/ja)
- [GitHub入門ガイド](https://guides.github.com/)
- [GitHubの使い方まとめ](https://qiita.com/items/656deb8d8cdf13fd590c)

Happy Coding! 🚀 

