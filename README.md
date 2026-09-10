# naorex.link

`https://naorex.link/` 用のシンプルなGitHub Pagesポータルです。

ビルドツールやフレームワークを使わず、HTML/CSSだけで管理します。

## Files

```text
.
├── .hallmark/
│   ├── log.json
│   └── preflight.json
├── CNAME
├── about.html
├── apps/
│   └── luck-wealth-simulator.html
├── docs/
│   └── history/
├── index.html
├── privacy.html
├── robots.txt
├── sitemap.xml
├── styles.css
├── tokens.css
├── ads.txt
└── README.md
```

`about.html` はサイトの目的と運営方針、
`apps/luck-wealth-simulator.html` は公開アプリの仕組み、操作方法、
結果指標、モデルの限界を説明する詳細解説を掲載します。
配色、タイポグラフィ、余白などのデザイントークンは `tokens.css` で管理します。

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

## Search engines

`robots.txt` では、クローラーに公開ページのクロールを許可し、
`sitemap.xml` の場所を案内しています。

`sitemap.xml` には、現在公開しているページのURLだけを掲載します。
公開ページを追加、移動、削除した場合は、サイトマップも同時に更新してください。

公開後、次のURLで内容を直接確認できます。

```text
https://naorex.link/robots.txt
https://naorex.link/sitemap.xml
```

## Cloudflare DNS

Cloudflare側では `naorex.link` のDNSを管理し、
apex (`@`) をGitHub Pagesへ向けます。

GitHub Pagesが案内する最新のDNS設定値を確認したうえで設定してください。

CloudflareのProxy設定については、最初は `DNS only` で
GitHub Pages側のHTTPS設定を確認するのが分かりやすいです。

## Google AdSense

### 1. AdSense script

`privacy.html` の `<head>` に、
AdSense script のテンプレートをコメントで置いています。

AdSenseで発行された実際のコードを使用し、

```text
ca-pub-XXXXXXXXXXXXXXXX
```

を自分のPublisher IDに置き換えてコメントを解除してください。

### 2. ads.txt

`ads.txt` には AdSense 管理画面の `Ads.txt スニペット` を設定しています。
Publisher ID を変更した場合は、AdSense 管理画面に表示される1行で更新してください。

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

## About and app pages

`about.html` には、サイトの目的、公開するコンテンツ、運営方針、
GitHubを通じた連絡方法を記載しています。

`apps/luck-wealth-simulator.html` は Luck Wealth Simulator の詳細解説ページです。
操作できる条件、結果の読み方、富が偏る理由、再分配の働き、
モデルが扱わない現実の要因を説明します。
公開中のアプリ本体は次のURLで提供します。

```text
https://luck-wealth-simulator.naorex.link/
```

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
