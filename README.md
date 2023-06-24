# zsh-romaji-complete

zshのタブ補完でローマ字による日本語ファイル名補完ができるようにします。

例: `niho<Tab>` で`日本`で始まるファイル名が補完されます。

<img src="./demo.gif">

## セットアップ

### 1. このリポジトリをクローン

お好きな場所にクローンします:

```console
$ git clone git@github.com:aoyama-val/zsh-romaji-complete.git
```

### 2. kakasiをインストール

```console
$ git clone --depth 1 git@github.com:loretoparisi/kakasi.git
$ cd kakasi
$ ./configure && make && make install
```

### 3. `~/.zshrc`に下記を追加:

```
bindkey "^I" menu-expand-or-complete
export ZSH_ROMAJI_COMPLETE_HOME={このリポジトリのディレクトリ}
. "${ZSH_ROMAJI_COMPLETE_HOME}/init.zsh"
```

zshのデフォルトでは `^I` は `expand-or-complete`ですが、それだと候補が複数ある場合に何も補完されません。

### 4. シェルを再起動

再起動すると補完ができるようになっています。
