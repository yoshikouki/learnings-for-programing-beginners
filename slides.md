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
4. あなただけの入門方法がある
5. 入門のための良さそうな教材
6. 発展するのに良さそうな教材
7. 作ってみたいものがないときの例題
8. 聞ける人いることは恵まれているので活用しましょう
9. 出典

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
4. あなただけの入門方法がある
5. 入門のための良さそうな教材
6. 発展するのに良さそうな教材
7. 作ってみたいものがないときの例題
8. 聞ける人いることは恵まれているので活用しましょう
9. 出典

---

# JavaScript とは

> JavaScript (JS) は軽量で、インタープリター型、あるいは実行時コンパイルされる、第一級関数を備えたプログラミング言語です。ウェブページでよく使用されるスクリプト言語として知られ、多くの非ブラウザー環境、例えば Node.js や Apache CouchDB や Adobe Acrobat などでも使用されています。 JavaScript はプロトタイプベースで、シングルスレッドで、動的型付けを持ち、そしてオブジェクト指向、命令型、宣言型 (関数プログラミングなど) といったスタイルをサポートするマルチパラダイムのスクリプト言語です。詳しくは JavaScript についてをお読みください。
>
> https://developer.mozilla.org/ja/docs/Web/JavaScript

---

# 1. フロントエンドの JavaScript

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

# 1. フロントエンドの JavaScript

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

# 1. フロントエンドの JavaScript

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

# 1. フロントエンドの JavaScript フレームワーク

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

---

# 1. フロントエンドの JavaScript ライブラリ

- [jQuery](https://jquery.com/)
- [React](https://ja.reactjs.org/)
- [Vue.js](https://jp.vuejs.org/) (本家はフレームワークと表現)

---

## 2. バックエンドの JavaScript

---

# あなただけの入門方法がある

---

# 入門のための良さそうな教材

---

# 発展するのに良さそうな教材

---

# 作ってみたいものがないときの例題

---

# 聞ける人いることは恵まれているので活用しましょう

---

# 出典
