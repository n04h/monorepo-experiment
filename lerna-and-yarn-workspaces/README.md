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
// or
yarn workspace @<root-package-name>/<package-name> add form-data
```

### 共通ライブラリのインストール

```sh
yarn add -W --dev typescript prettier eslint
```
