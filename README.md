This is a [Plasmo extension](https://docs.plasmo.com/) project bootstrapped with [`plasmo init`](https://www.npmjs.com/package/plasmo).

pnpmが入っていない場合はinstallしてください.
https://pnpm.io/installation

# Version

- pnpm 8.10.0

## 開発方法

pnpm-lock.yamlからnode_modulesを作成

```
pnpm i --frozen-lockfile
```

起動

```bash
pnpm dev
```

`pnpm dev`を実行すると`build`フォルダの中に`chrome-mv3-dev`というフォルダが作成されます。

作成されたら、[chrome://extensions](chrome://extensions)を開いて右上にある`Developer mode`をOnにします。

「パッケージ化されていない拡張機能を読み込む」ボタンをクリックして、`chrome-mv3-dev`を読み込みます。

ホットリロードに対応しています。

詳細は下記URLを参照してください。
https://docs.plasmo.com/framework#loading-the-extension-in-chrome

## Making production build

Run the following:

```bash
pnpm build
```

This should create a production bundle for your extension, ready to be zipped and published to the stores.

## zip package

```
pnpm package
```

## test

using jest

```
pnpm test
```

## story

using ladle

```
pnpm ladle
```

## Submit to the webstores

The easiest way to deploy your Plasmo extension is to use the built-in [bpp](https://bpp.browser.market) GitHub action. Prior to using this action however, make sure to build your extension and upload the first version to the store to establish the basic credentials. Then, simply follow [this setup instruction](https://docs.plasmo.com/framework/workflows/submit) and you should be on your way for automated submission!

