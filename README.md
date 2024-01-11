# practice-vite

## Commands

### npm create

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

### npm install && npm run dev

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

## npm run build && npm run preview

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
```

## References

- [改訂3版JavaScript本格入門 ～モダンスタイルによる基礎から現場での応用まで：書籍案内｜技術評論社](https://gihyo.jp/book/2023/978-4-297-13288-0)
- [Vite | 次世代フロントエンドツール](https://ja.vitejs.dev/)
    - [静的サイトのデプロイ | Vite](https://ja.vitejs.dev/guide/static-deploy.html)
    - [Vite の設定 | Vite](https://ja.vitejs.dev/config/)
    - [共通オプション | Vite](https://ja.vitejs.dev/config/shared-options.html)
