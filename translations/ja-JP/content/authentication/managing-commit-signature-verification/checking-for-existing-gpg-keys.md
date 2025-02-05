---
title: 既存の GPG キーの確認
intro: GPG キーを生成する前に、GPG キーがすでに存在するかどうかを確認できます。
redirect_from:
  - /articles/checking-for-existing-gpg-keys
  - /github/authenticating-to-github/checking-for-existing-gpg-keys
  - /github/authenticating-to-github/managing-commit-signature-verification/checking-for-existing-gpg-keys
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
shortTitle: Existing GPG keys
---

{% data reusables.gpg.supported-gpg-key-algorithms %}

{% note %}

**注釈:** デフォルト設定では、macOS や Windows に GPG はインストールされていません。 GPG コマンドラインツールをインストールするには、[GnuPG のダウンロードページ](https://www.gnupg.org/download/)を参照してください。

{% endnote %}

{% data reusables.command_line.open_the_multi_os_terminal %}
{% data reusables.gpg.list-keys-with-note %}
3. コマンドの出力結果を見て、GPG キーペアがあるか確認します。
    * GPG キーのペアが存在しないか、既存の GPG キーをコミットやタグへの署名に利用したくない場合、[新しい GPG キーを作成](/articles/generating-a-new-gpg-key)します。
    * If there's an existing GPG key pair and you want to use it to sign commits and tags, you can display the public key using the following command, substituting in the GPG key ID you'd like to use. この例では、GPG キー ID は `3AA5C34371567BD2` です。
      ```shell
      $ gpg --armor --export <em>3AA5C34371567BD2</em>
      # Prints the GPG key ID, in ASCII armor format
      ```
      You can then [add your GPG key to your GitHub account](/articles/adding-a-gpg-key-to-your-github-account).

## 参考リンク

* [新しい GPG キーの生成](/articles/generating-a-new-gpg-key)
* "[Adding a GPG key to your GitHub account](/articles/adding-a-gpg-key-to-your-github-account)"
* 「[Git へ署名キーを伝える](/articles/telling-git-about-your-signing-key)」
* [GPG キーとメールの関連付け](/articles/associating-an-email-with-your-gpg-key)
* 「[コミットに署名する](/articles/signing-commits)」
* 「[タグに署名する](/articles/signing-tags)」
