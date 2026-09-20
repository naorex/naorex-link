# Design — naorex.link

このサイトの固定デザインシステムです。すべてのページは、個別の装飾より先にこの文書と `tokens.css` を参照します。ページ固有の変更が必要な場合も、ローカルな上書きを増やすのではなく、先にこの文書へ許容範囲を追記します。

## Genre

Editorial。個人で作ったWebアプリと、それを理解するための読み物を、静かな編集誌のように見せます。

## Macrostructure family

- ポータル: Split Studio。短いサイト説明と、アプリ／ブログの具体的な情報を非対称の2列で組みます。
- アプリ解説: 共通のGuide shell。導入、事実一覧、ページ内索引、長文セクションを共有し、実画面があるページだけWorkbenchの図版を許可します。
- 読み物・規約: Long Document。Blog、About、Privacyは本文幅、見出し間隔、リンク表現を共有します。

## Theme

- `--color-paper`: `oklch(97.5% 0.004 115)`
- `--color-paper-2`: `oklch(99% 0.003 115)`
- `--color-paper-3`: `oklch(94.5% 0.008 115)`
- `--color-ink`: `oklch(20% 0.008 150)`
- `--color-ink-2`: `oklch(31% 0.009 150)`
- `--color-muted`: `oklch(49% 0.012 150)`
- `--color-rule`: `oklch(88% 0.01 115)`
- `--color-rule-2`: `oklch(72% 0.014 120)`
- `--color-accent`: `oklch(43% 0.09 158)`
- `--color-focus`: `oklch(55% 0.13 158)`

深緑は主CTA、リンク、現在地、フォーカスへ限定し、各ビューポートの5%未満に抑えます。背景は純白、本文は純黒にしません。

## Typography

- Display: Noto Serif JP、700、normal。ページタイトル、セクション見出し、カードタイトル、ワードマークに使用します。
- Body: Noto Sans JP、400。本文、ナビゲーション、注釈、UIに使用します。
- Emphasis: Noto Sans JP、700。ボタン、定義語、短いUIラベルに使用します。
- Display tracking: `-0.035em`
- Type scale anchor: `--text-display: clamp(3rem, 7vw, 5.25rem)`
- Portal title: `--text-portal: clamp(2rem, 5vw, 3.75rem)`

見出しはitalicにせず、本文は45〜75字幅、行高1.7前後を基準にします。英字と日本語も同じ2書体の中で組みます。

## Spacing

4pxを基準にした名前付きスケールを `tokens.css` で管理します。ページ内では生の色値、書体名、任意の余白値を追加せず、必ずトークンを参照します。

## Navigation and footer

- Navigation: N6 Newspaper masthead。架空の号数や日付は置かず、中央のワードマーク、共通ナビ、二重罫線で構成します。
- 共通ナビ順: Apps / Blog / About / Privacy / GitHub。Homeはワードマークが担います。
- Footer: Ft1 Mast-headed。ワードマーク、著作権、共通リンクだけを置き、ページ固有CTAは本文内に残します。

## Motion

- ページロードやスクロール連動の演出は使いません。
- 主CTAはhoverで1px上がり、activeで元へ戻ります。
- 色とtransformだけを、名前付きdurationとeasingで遷移させます。
- `prefers-reduced-motion` では空間移動を止め、遷移を150ms以下にします。

## CTA voice

- Primary: 深緑の塗り、短い動詞ラベル、1行、44px以上の操作領域。
- Secondary: 下線付きの文字リンク。primaryと同じ強さで競合させません。
- focus-visibleは即時表示し、2px以上かつ3:1以上のコントラストを確保します。

## Per-page allowances

- トップは、既存のアプリ／ブログ紹介カードと2列構造を維持できます。
- アプリ解説は、実在するプロダクト画面だけを図版として使用できます。
- Blog、About、Privacyはタイポグラフィ中心とし、装飾画像を追加しません。
- 潮位なびの既存キャプチャ以外に、画像や実績値を新しく作りません。

## What pages must share

- ワードマーク、マストヘッド、ナビ順、フッター構造
- Gardenパレットとアクセントの使い方
- Display／Bodyの2書体と文字サイズ階層
- 主CTAと副導線の形、フォーカス表現
- ページ導入、本文幅、罫線、余白のリズム

## What pages may differ on

- トップ、アプリ解説、長文ページそれぞれの情報配置
- 実画面キャプチャの有無
- ページ内索引と事実一覧の項目数

## Exports

### tokens.css

```css
:root {
  --color-paper: oklch(97.5% 0.004 115);
  --color-paper-2: oklch(99% 0.003 115);
  --color-paper-3: oklch(94.5% 0.008 115);
  --color-ink: oklch(20% 0.008 150);
  --color-ink-2: oklch(31% 0.009 150);
  --color-muted: oklch(49% 0.012 150);
  --color-rule: oklch(88% 0.01 115);
  --color-rule-2: oklch(72% 0.014 120);
  --color-accent: oklch(43% 0.09 158);
  --color-accent-hover: oklch(35% 0.075 158);
  --color-accent-ink: oklch(98% 0.004 115);
  --color-focus: oklch(55% 0.13 158);

  --font-display: "Noto Serif JP", "Yu Mincho", "Hiragino Mincho ProN", serif;
  --font-body: "Noto Sans JP", "Hiragino Sans", "Yu Gothic", sans-serif;

  --space-3xs: 0.125rem;
  --space-2xs: 0.25rem;
  --space-xs: 0.5rem;
  --space-sm: 0.75rem;
  --space-md: 1rem;
  --space-lg: 1.5rem;
  --space-xl: 2.5rem;
  --space-2xl: 4rem;
  --space-3xl: 6rem;
  --space-4xl: 9rem;

  --text-xs: 0.75rem;
  --text-sm: 0.875rem;
  --text-base: 1rem;
  --text-md: 1.125rem;
  --text-lg: 1.375rem;
  --text-xl: 1.75rem;
  --text-2xl: 2.25rem;
  --text-3xl: 3rem;
  --text-4xl: 3.75rem;
  --text-display: clamp(3rem, 7vw, 5.25rem);
  --text-portal: clamp(2rem, 5vw, 3.75rem);

  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in: cubic-bezier(0.7, 0, 0.84, 0);
  --ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);
  --dur-micro: 120ms;
  --dur-short: 220ms;
  --dur-long: 420ms;

  --rule-hair: 1px;
  --rule-fine: 2px;
  --radius-card: 1rem;
  --radius-pill: 999px;
  --radius-input: 0.75rem;
}
```

### Tailwind v4 `@theme`

```css
@theme {
  --color-paper: oklch(97.5% 0.004 115);
  --color-paper-2: oklch(99% 0.003 115);
  --color-paper-3: oklch(94.5% 0.008 115);
  --color-ink: oklch(20% 0.008 150);
  --color-ink-2: oklch(31% 0.009 150);
  --color-muted: oklch(49% 0.012 150);
  --color-rule: oklch(88% 0.01 115);
  --color-rule-2: oklch(72% 0.014 120);
  --color-accent: oklch(43% 0.09 158);
  --color-focus: oklch(55% 0.13 158);
  --font-display: "Noto Serif JP", serif;
  --font-body: "Noto Sans JP", sans-serif;
  --spacing-3xs: 0.125rem;
  --spacing-2xs: 0.25rem;
  --spacing-xs: 0.5rem;
  --spacing-sm: 0.75rem;
  --spacing-md: 1rem;
  --spacing-lg: 1.5rem;
  --spacing-xl: 2.5rem;
  --spacing-2xl: 4rem;
  --text-xs: 0.75rem;
  --text-sm: 0.875rem;
  --text-md: 1.125rem;
  --text-lg: 1.375rem;
  --text-xl: 1.75rem;
  --text-2xl: 2.25rem;
  --text-portal: clamp(2rem, 5vw, 3.75rem);
  --radius-card: 1rem;
  --radius-pill: 999px;
  --radius-input: 0.75rem;
  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in: cubic-bezier(0.7, 0, 0.84, 0);
  --ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);
}
```

### DTCG `tokens.json`

```json
{
  "$schema": "https://design-tokens.github.io/community-group/format/",
  "color": {
    "paper": { "$value": "oklch(97.5% 0.004 115)", "$type": "color" },
    "paper-2": { "$value": "oklch(99% 0.003 115)", "$type": "color" },
    "paper-3": { "$value": "oklch(94.5% 0.008 115)", "$type": "color" },
    "ink": { "$value": "oklch(20% 0.008 150)", "$type": "color" },
    "ink-2": { "$value": "oklch(31% 0.009 150)", "$type": "color" },
    "muted": { "$value": "oklch(49% 0.012 150)", "$type": "color" },
    "rule": { "$value": "oklch(88% 0.01 115)", "$type": "color" },
    "rule-2": { "$value": "oklch(72% 0.014 120)", "$type": "color" },
    "accent": { "$value": "oklch(43% 0.09 158)", "$type": "color" },
    "focus": { "$value": "oklch(55% 0.13 158)", "$type": "color" }
  },
  "font": {
    "display": { "$value": "Noto Serif JP, Yu Mincho, serif", "$type": "fontFamily" },
    "body": { "$value": "Noto Sans JP, Yu Gothic, sans-serif", "$type": "fontFamily" }
  },
  "size": {
    "portal": { "$value": "3.75rem", "$type": "dimension" }
  },
  "space": {
    "xs": { "$value": "0.5rem", "$type": "dimension" },
    "sm": { "$value": "0.75rem", "$type": "dimension" },
    "md": { "$value": "1rem", "$type": "dimension" },
    "lg": { "$value": "1.5rem", "$type": "dimension" },
    "xl": { "$value": "2.5rem", "$type": "dimension" },
    "2xl": { "$value": "4rem", "$type": "dimension" }
  },
  "duration": {
    "micro": { "$value": "120ms", "$type": "duration" },
    "short": { "$value": "220ms", "$type": "duration" },
    "long": { "$value": "420ms", "$type": "duration" }
  }
}
```

### shadcn/ui CSS variables

```css
:root {
  --background: 97.5% 0.004 115;
  --foreground: 20% 0.008 150;
  --card: 99% 0.003 115;
  --card-foreground: 20% 0.008 150;
  --popover: 99% 0.003 115;
  --popover-foreground: 20% 0.008 150;
  --primary: 43% 0.09 158;
  --primary-foreground: 98% 0.004 115;
  --secondary: 94.5% 0.008 115;
  --secondary-foreground: 31% 0.009 150;
  --muted: 88% 0.01 115;
  --muted-foreground: 49% 0.012 150;
  --accent: 43% 0.09 158;
  --accent-foreground: 98% 0.004 115;
  --border: 88% 0.01 115;
  --input: 88% 0.01 115;
  --ring: 55% 0.13 158;
  --radius: 1rem;
}
```
