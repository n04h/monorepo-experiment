# LernaとYarn WorkspacesでのMonorepo

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
yarn lerna publish <patch | minor | major>
```
