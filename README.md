# homebrew-meltype-for-mac

[Meltype for Mac](https://github.com/whitewater-png/Meltype-for-Mac) の Homebrew tap です (本家 Meltype とは別の、Mac 版フォークの配布です)。

```sh
brew install --cask whitewater-png/meltype-for-mac/meltype-for-mac
```

インストール後は、いったんログアウトしてログインし直してください (Homebrew の処理はサンドボックスの中で動くため、入力ソースの登録を済ませられません)。そのあと、メニューバーの入力メニューで「Meltype」を選びます。

- 既に `~/Library/Input Methods/Meltype.app` (zip や開発版) があるときは、先に外してから入れてください (Homebrew は上書きしません)。
- 更新: `brew upgrade --cask meltype-for-mac`。アプリ内の「新しい版があります」の通知は Homebrew の版と食い違うことがあります。
- 削除: `brew uninstall --cask meltype-for-mac`。設定・学習データ (`~/Library/Application Support/Meltype`) も消すときは `--zap` を付けます (ユーザー辞書は先に控えを取ってください)。
- 署名は ad-hoc で、Apple の公証は受けていません。cask は Release の zip の SHA-256 を検証し、インストール後に quarantine 属性を外します (そのままだと macOS が IME を黙って止めるため)。

cask の正本は本体リポジトリの `mac/homebrew/Casks/meltype-for-mac.rb` にあり、版ごとにここへ写しています。不具合は本体リポジトリの [Issues](https://github.com/whitewater-png/Meltype-for-Mac/issues) へお願いします。
