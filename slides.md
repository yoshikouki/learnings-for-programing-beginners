---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: "text-center"
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: true
# some information about the slides, markdown enabled
info: |
  ref: https://github.com/yoshikouki/learnings-for-programing-beginners
# persist drawings in exports and build
drawings:
  persist: false
---

# JavaScript 入門ガイド

学生やプログラミング初学者が<br>
JavaScript に入門するためのガイド

---

# 目次

1. 自己紹介
2. 本日のゴール
3. JavaScript とは
   1. フロントエンドの JavaScript
   2. バックエンドの JavaScript
   3. その他 (AltJS・ビルドツール・ネイティブアプリ)
4. あなただけの入門方法がある
5. 入門のための良さそうな教材
6. 発展するのに良さそうな教材
7. 作ってみたいものがないときの例題
8. 聞ける人いることは恵まれているので活用しましょう

---

# @yoshikouki\_

- yoshikouki.eth.xyz

<img src="https://secure.gravatar.com/avatar/a6c581d156d86d79ea83cbbccdfebbe0?s=300&d=mm&r=g" class="my-4 h-40 rounded shadow" />

<img src="QRcode-twitter.png" class="h-40 rounded shadow" />

---

# 本日のゴール

- JavaScript を勉強する上で、知っておいたほうがいい全体感やキーワードの関係性を掴む
- 「こういうのを作りたい」となったときに、何を調べたら良いかが分かるようになる

## 本日話さないこと

- JavaScript の文法など

---

# 目次

1. 自己紹介
2. 本日のゴール
3. **JavaScript とは**
   1. フロントエンドの JavaScript
   2. バックエンドの JavaScript
   3. その他 (AltJS・ビルドツール・ネイティブアプリ)
4. あなただけの入門方法がある
5. 入門のための良さそうな教材
6. 発展するのに良さそうな教材
7. 作ってみたいものがないときの例題
8. 聞ける人いることは恵まれているので活用しましょう

---

# JavaScript とは

> JavaScript (JS) は軽量で、インタープリター型、あるいは実行時コンパイルされる、第一級関数を備えたプログラミング言語です。ウェブページでよく使用されるスクリプト言語として知られ、多くの非ブラウザー環境、例えば Node.js や Apache CouchDB や Adobe Acrobat などでも使用されています。 JavaScript はプロトタイプベースで、シングルスレッドで、動的型付けを持ち、そしてオブジェクト指向、命令型、宣言型 (関数プログラミングなど) といったスタイルをサポートするマルチパラダイムのスクリプト言語です。詳しくは JavaScript についてをお読みください。
>
> https://developer.mozilla.org/ja/docs/Web/JavaScript

---

# JavaScript とは

<div class="grid grid-cols-2 gap-4">
<div>

### HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
  </head>

  <body>
    <h1>Hello, world!</h1>
  </body>
</html>
```

</div>
<div>

<h1>Hello, world!</h1>

</div></div>

---

# JavaScript とは

<div class="grid grid-cols-2 gap-4">
<div>

### HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
  </head>

  <body>
    <h1>Hello, world!</h1>
  </body>
</html>
```

### CSS

```css
h1 {
  color: red;
  font-weight: bold;
}
```

</div>
<div>

<h1 class="text-red-500 font-bold">Hello, world!</h1>

</div></div>

---

# JavaScript とは

<div class="grid grid-cols-2 gap-4">
<div>

### HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
  </head>

  <body>
    <h1 id="js-clicker">Hello, world!</h1>
  </body>
</html>
```

### CSS

```css
h1 {
  color: red;
  font-weight: bold;
}
```

</div>
<div>

<h1 id="js-clicker" class="text-red-500 font-bold">Hello, world!</h1>

<Counter :count="10" m="t-4" />

### JavaScript

```js
const clicker = document.getElementById("js-clicker");
clicker.addEventListener("click", () => {
  clicker.innerText += "!";
});
```

</div></div>

---

# 目次

1. 自己紹介
2. 本日のゴール
3. JavaScript とは
   1. **フロントエンドの JavaScript**
   2. **バックエンドの JavaScript**
   3. **その他 (AltJS・ビルドツール・ネイティブアプリ)**
4. あなただけの入門方法がある
5. 入門のための良さそうな教材
6. 発展するのに良さそうな教材
7. 作ってみたいものがないときの例題
8. 聞ける人いることは恵まれているので活用しましょう

---

# ライブラリとフレームワーク

<div class="grid grid-cols-2 gap-4">
<div>

> アプリケーションを開発するとき、その土台として機能させるソフトウェアのこと。「アプリケーションフレームワーク」とも呼ばれる。「枠組み」「骨組み」「構造」などといった意味があり、土台となるフレームワークに必要な機能を追加し、アプリケーションの開発を進めていくのが一般的。
>
> .
>
> .
>
> .
>
> フレームワークの最大のメリットは、目的のアプリケーションをゼロから開発する必要がないので、開発工程を大幅に短縮できることにある。その反面、フレームワーク特有のコードがあるために、プログラミング言語に加え、そのコードを覚えなければならないという欠点もある。

https://www.otsuka-shokai.co.jp/words/framework.html

</div>
<div>

<img src="library-and-framework.png" class="rounded shadow" />

https://shura.design/2020/08/15/archives/2817

</div>
</div>

---

# 1. フロントエンドの JavaScript

- Vanilla JavaScript (素の JS)
- [jQuery](https://jquery.com/)
- [React](https://ja.reactjs.org/)
- [Vue.js](https://jp.vuejs.org/) (本家はフレームワークと表現)
- [Angular](https://angular.io/)
- [Svelte](https://svelte.jp/)

[Google トレンド](https://trends.google.co.jp/trends/explore?date=today%205-y&geo=JP&q=React,Vue,Angular)

---

# 1. フロントエンドの JavaScript フレームワーク

- [Next.js](https://nextjs.org/) for React
- [Nuxt.js](https://nuxtjs.org/) for Vue

[Google トレンド](https://trends.google.co.jp/trends/explore?date=today%205-y&geo=JP&q=Next.js,Nuxt.js)

[海外最新アンケートを見てみましょう (Netflix, AWS, Cloudflare)](https://tsh.io/state-of-frontend/)

---

## 2. バックエンドの JavaScript

- JavaScript は一般的にブラウザで動くもの
- その JavaScript をブラウザ外で動くようにしたランタイム (実行環境)
  - どちらも V8 という JavaScript engine を使用している
- [Node.js](https://nodejs.org/ja/)
- [Deno](https://deno.land/) (TypeScript もそのまま実行してくれる)

フレームワーク

- [Express](https://expressjs.com/ja/) for Node.js
- [Nest.js](https://nestjs.com/) for Node.js

ORM (Object-Relational Mapping)

- [Prisma](https://www.prisma.io/)
- [TypeORM](https://typeorm.io/)

---

## 3. その他 - AltJS

- [TypeScript](https://www.typescriptlang.org/)
- [CoffeeScript](https://coffeescript.org/)

---

## 3. その他 - ビルドツール

- [Vite](https://ja.vitejs.dev/)
- [Webpack](https://webpack.js.org/)
- [Babel](https://babeljs.io/)

---

## 3. その他 - ネイティブアプリ

- [React Native](https://reactnative.dev/) for スマホ
- [electronJS](https://www.electronjs.org/) for PC

---

# 目次

1. 自己紹介
2. 本日のゴール
3. JavaScript とは
   1. フロントエンドの JavaScript
   2. バックエンドの JavaScript
   3. その他 (AltJS・ビルドツール・ネイティブアプリ)
4. **あなただけの入門方法がある**
5. **入門のための良さそうな教材**
6. **発展するのに良さそうな教材**
7. 作ってみたいものがないときの例題
8. 聞ける人いることは恵まれているので活用しましょう

---

# あなただけの入門方法がある

まず入門するゴールを明確にしましょう！

- 「プログラミングを体験してみたい」
- 「プログラミング的な思考を身に着けたい」
- 「Google Spreadsheet を自動化したい」
- 「サービスを作ってみたい」

その後、入門方法にも得意・不得意があるので自分に合う方を選択したら良い

<div class="grid grid-cols-2 gap-4 my-10">
<div>

最初から知識を体系的に身につける

ex) 体系的な入門書、良質なネット情報など

</div>
<div>

実践しつつ、必要な知識を身に着けていく

ex) ワークショップ、サンプルアプリ制作、個人サービス開発など

</div>
</div>

---

# 入門のための良さそうな教材

- [Progate](https://prog-8.com/)
- [MDN web docs](https://developer.mozilla.org/ja/docs/Learn)
- [JavaScript Primer](https://jsprimer.net/)

無料なものをピックアップ

※ 全部やる必要ないし、読んでいて面白くないなら続かないので別の方法に切り替えてもいいかも

やっていて面白いことをやりましょう！

---

# 発展するのに良さそうな教材

- [web.dev](https://web.dev/)
- [roadmap.sh](https://roadmap.sh/)
- 各ライブラリ・フレームワークのチュートリアル or ドキュメント
- [競技プログラミング (リンクは問題 10 選の記事)](https://qiita.com/drken/items/fd4e5e3630d0f5859067)

※ 全部やる必要ないし、読んでいて面白くないなら続かないので別の方法に切り替えてもいいかも

やっていて面白いことをやりましょう！

---

# 目次

1. 自己紹介
2. 本日のゴール
3. JavaScript とは
   1. フロントエンドの JavaScript
   2. バックエンドの JavaScript
   3. その他 (AltJS・ビルドツール・ネイティブアプリ)
4. あなただけの入門方法がある
5. 入門のための良さそうな教材
6. 発展するのに良さそうな教材
7. **作ってみたいものがないときの例題**
8. 聞ける人いることは恵まれているので活用しましょう

---

# 自分で思いついたものを作ってみる

- 生活のちょっとした「めんどくさい」は制作物のヒントになる
- いつも使っているサービスの「こういうのあったら良いのにな」というのもいい
  - 毎朝、桜島の灰が来そうか LINE で連絡する

---

# 作ってみたいものを思いつかないときの例題

---

<div class="grid grid-cols-3 gap-4">
<div>

<Tweet id="1522539189958369280"/>

</div>
<div>

<Tweet id="1522539197566885889"/>

</div>
<div>

<Tweet id="1522539204391043075"/>

</div>
</div>

---

# 目次

1. 自己紹介
2. 本日のゴール
3. JavaScript とは
   1. フロントエンドの JavaScript
   2. バックエンドの JavaScript
   3. その他 (AltJS・ビルドツール・ネイティブアプリ)
4. あなただけの入門方法がある
5. 入門のための良さそうな教材
6. 発展するのに良さそうな教材
7. 作ってみたいものがないときの例題
8. **聞ける人いることは恵まれているので活用しましょう**

---

# 聞ける人いることは恵まれているので活用しましょう

- エンジニアリングを知っている人のコミュニティに属していることは実は恵まれている
- 「反応ないかもしれんけどまあ一旦やってみっか」くらいの気持ちで質問してみましょう！
- 私に力になれそうなことがありましたら気軽にお声がけください〜
