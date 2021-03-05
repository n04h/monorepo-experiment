# lernaとyarn workspacesでのmonorepo

lernaだけでは各パッケージへの外部パッケージの追加がyarn経由の直感的な方法で行えないため、
yarn workspacesと合わせて使ったmonorepoのサンプル。

## 使用バージョン

yarn: 1.22.10
lerna: 3.22.1

## チートシート

### パッケージ追加

```sh
yarn lerna create @<root-package-name>/<package-name>
```

### 各パッケージへのライブラリインストール

ルートディレクトリのyarn.lockで

```sh
cd packages/<package-name>
yarn add form-data
```

または

```sh
yarn workspace @<root-package-name>/<package-name> add form-data
```

### 共通ライブラリのインストール

```sh
yarn add -W --dev typescript prettier eslint
```

### パブリッシュ

オプションでバージョンアップの指定ができる
新しいパッケージの場合は`from-package`を追記する

```sh
yarn lerna publish
```
