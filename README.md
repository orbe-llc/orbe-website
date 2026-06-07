# orbe-website

orbe合同会社のコーポレートサイト。法人口座開設の実在性証明と、屋号の正面玄関を兼ねる静的1ページ。

## What

`index.html` 1枚の静的サイト。依存ゼロ、ビルド不要。会社実在情報（商号・所在地・代表者・設立・事業内容）を掲載する。

## How

GitHub Pages でホストする。`main` に push すると自動でデプロイされる。

- 独自ドメイン: `orbe.co.jp`（apex）— `CNAME` ファイルで設定
- DNS: お名前.com で apex に A レコード4本を追加（GitHub Pages の固定IP）。MX/TXT は Google Workspace 用なので一切変更しない
- SSL: GitHub Pages が Let's Encrypt で自動発行

### お名前.com に追加する A レコード（apex / ホスト名空欄）

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

`www` を使うなら CNAME `www → 168masaki.github.io` を別途追加する（任意・拡張）。

## Why

GMOあおぞらネット銀行の法人口座審査で、HP の有無が実在性確認に効く。完全無料・SSL自動・apex対応の GitHub Pages を選択した。
