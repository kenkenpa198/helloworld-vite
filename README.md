<!-- omit in toc -->
# practice-vite

## 1. Commands

### 1.1. npm create

```shell
$ npm create vite@latest
✔ Project name: … practice-vite
✔ Select a framework: › Vanilla
✔ Select a variant: › JavaScript
...
Done. Now run:

  cd practice-vite
  npm install
  npm run dev
```

### 1.2. npm install && npm run dev

```shell
$ cd practice-vite
$ npm install

added 11 packages, and audited 12 packages in 1s

3 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

$ npm run dev

> practice-vite@0.0.0 dev
> vite


  VITE v5.0.11  ready in 120 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
```

### 1.3. npm run build && npm run preview

```shell
$ npm run build

> practice-vite@0.0.0 build
> vite build

vite v5.0.11 building for production...
✓ 7 modules transformed.
dist/index.html                 0.45 kB │ gzip: 0.29 kB
dist/assets/index-X4m0RMh6.css  1.21 kB │ gzip: 0.63 kB
dist/assets/index-xf4JlvXi.js   2.59 kB │ gzip: 1.38 kB
✓ built in 87ms

$ npm run preview

> practice-vite@0.0.0 preview
> vite preview

  ➜  Local:   http://localhost:4173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
```

## 2. Deploy by GitHub Pages

公開ページ: [https://kenkenpa198.github.io/practice-vite/](https://kenkenpa198.github.io/practice-vite/)

1. プロジェクトルートへ `vite.config.js` を作成する。

    ```shell
    cd practice-vite
    touch vite.config.js
    ```

    参考) [Vite の設定 | Vite](https://ja.vitejs.dev/config/)

2. 下記の通り記述する。

    ```js
    export default {
        base: '/practice-vite/',
    }
    ```

    参考) [共通オプション | Vite](https://ja.vitejs.dev/config/shared-options.html)

3. GitHub Actions の設定ファイルを作成する。

    ```shell
    mkdir -p .github/workflows
    touch .github/workflows/main.yml
    ```

    参考) [kenkenpa198/practice-github-actions](https://github.com/kenkenpa198/practice-github-actions)

4. `main.yml` へ [静的サイトのデプロイ | Vite](https://ja.vitejs.dev/guide/static-deploy.html#github-pages) > [GitHub Pages](https://ja.vitejs.dev/guide/static-deploy.html#github-pages) 上のサンプルコードを記述する。

    ```yml
    # 静的コンテンツを GitHub Pages にデプロイするためのシンプルなワークフロー
    name: Deploy static content to Pages
    ...
    ```

5. GitHub リポジトリページ > `Settings` > `Pages` へ遷移する。
6. `Build and deployment` > `Source` のプルダウンメニューから `GitHub Actions` を選択する。
7. プッシュする。
8. main ブランチの状態でビルド ～ デプロイが行われたことを確認する。

## 3. References

- [改訂3版JavaScript本格入門 ～モダンスタイルによる基礎から現場での応用まで：書籍案内｜技術評論社](https://gihyo.jp/book/2023/978-4-297-13288-0)
- [Vite | 次世代フロントエンドツール](https://ja.vitejs.dev/)
    - [静的サイトのデプロイ | Vite](https://ja.vitejs.dev/guide/static-deploy.html)
    - [Vite の設定 | Vite](https://ja.vitejs.dev/config/)
    - [共通オプション | Vite](https://ja.vitejs.dev/config/shared-options.html)
