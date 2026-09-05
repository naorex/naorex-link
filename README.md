# naorex.link

`https://naorex.link/` 用のシンプルなGitHub Pagesポータルです。

ビルドツールやフレームワークを使わず、HTML/CSSだけで管理します。

## Files

```text
.
├── CNAME
├── index.html
├── privacy.html
├── styles.css
├── ads.txt
└── README.md
```

## GitHub Pages

GitHubリポジトリの:

1. `Settings`
2. `Pages`
3. `Build and deployment`
4. `Deploy from a branch`

から公開対象のブランチを設定します。

Custom domain には:

```text
naorex.link
```

を指定します。

`CNAME` ファイルにも `naorex.link` を設定済みです。

## Cloudflare DNS

Cloudflare側では `naorex.link` のDNSを管理し、
apex (`@`) をGitHub Pagesへ向けます。

GitHub Pagesが案内する最新のDNS設定値を確認したうえで設定してください。

CloudflareのProxy設定については、最初は `DNS only` で
GitHub Pages側のHTTPS設定を確認するのが分かりやすいです。

## Google AdSense

### 1. AdSense script

`index.html` と `privacy.html` の `<head>` に、
AdSense script のテンプレートをコメントで置いています。

AdSenseで発行された実際のコードを使用し、

```text
ca-pub-XXXXXXXXXXXXXXXX
```

を自分のPublisher IDに置き換えてコメントを解除してください。

### 2. ads.txt

`ads.txt` は誤ったPublisher IDで公開しないよう、
初期状態ではコメントのみになっています。

AdSense管理画面の `Ads.txt スニペット` から表示された1行をコピーし、
`ads.txt` に設定してください。

形式例:

```text
google.com, pub-0000000000000000, DIRECT, f08c47fec0942fa0
```

`pub-0000000000000000` は例なので、そのまま使用しないでください。

公開後、次のURLで内容を直接確認できます。

```text
https://naorex.link/ads.txt
```

## Privacy policy

`privacy.html` には、Google AdSenseを利用する場合を想定し、
Cookie、第三者配信広告、パーソナライズド広告、
アクセス情報などについて記載しています。

アクセス解析、問い合わせフォーム、ログイン機能などを追加した場合は、
実際のデータ処理に合わせて更新してください。

## Add another app

`index.html` の `.app-grid` 内に `article.app-card` を追加すれば、
新しいWebアプリをポータルへ追加できます。

例:

```html
<article class="app-card">
  <div>
    <p class="app-meta">TOOL</p>
    <h3>App Name</h3>
    <p>アプリの簡単な説明。</p>
  </div>

  <a
    class="button"
    href="https://example.naorex.link/"
    target="_blank"
    rel="noopener noreferrer">
    アプリを開く
    <span aria-hidden="true">↗</span>
  </a>
</article>
```
