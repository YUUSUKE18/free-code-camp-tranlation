![元記事](https://www.freecodecamp.org/news/react-background-image-tutorial-how-to-set-backgroundimage-with-inline-css-style/)

## React Background Image Tutorial – How to Set backgroundImage with Inline CSS Style

## React の背景画像設定チュートリアル　- インライン CSS で背景画像を設定する方法

React のインライン CSS で使える backgroundImage スタイルプロパティを設定する方法が、4 つあります。

このチュートリアルでは、サンプルコードとともに、4 つ、全ての方法をご紹介します。

### How to Set a Background Image in React Using an External URL

```
function App() {
  return (
    <div style={{
      backgroundImage: `url("https://via.placeholder.com/500")`
    }}>
      Hello World
    </div>
  );
}
```

上のコードは、<background-image: url(https://via.placeholder.com/500)>のスタイルが<div>要素に適用し、描画を行います。

### How to Set a Background Image in React From Your /src Folder

### ご自身の/src フォルダ配下から React での背景画像の設定方法

React を使い、アプリケーションを開発、そして、src/フォルダ内部の画像を持っているならば、最初に画像を取り込み、要素の背景として、配置します。

```
import React from "react";
import background from "./img/placeholder.png";

function App() {
  return (
    <div style={{ backgroundImage: `url(${background})` }}>
      Hello World
    </div>
  );
}

export default App;
```

Setting background image using imported image
ファイルに取り込んだ画像を用いて、画像として設定する方法

npm start コマンドにて、アプリケーションを起動するとき、React アプリケーションは、画像が見つからない場合、内部で画像が見つけられないとして、コンパイルに失敗したというエラーを表示し、ビルドを停止します。

この方法だと、アプリケーション上で、いかなる画像リンクも表示されません。上のコードにおいて、<backgroundImage>の値は、開発者が JavaScript の表記にて埋め込めるテンプレート文字を使っています。

### How to Set a Background Image in React Using the Relative URL Method

### 相対 URL の方法で、React 内で背景画像を設定する方法

Create React App コマンドで作成された React アプリケーションの public フォルダは、静的な画像などを追加するために使われます。public フォルダ内に配置したどのようなファイルもオンラインで、アクセスできます。

The public/ folder in Create React App can be used to add static assets into your React application. Any files you put inside the folder will be accessible online.

public フォルダ内部に、image.png ファイルを配置している場合、<your host address>/image.png にて、画像情報にアクセスできます。ローカル環境下で React アプリを動かしているとき、画像は、http://localhost:3000/image.png となります。

If you put an image.png file inside the public/ folder, you can access it at <your host address>/image.png. When running React in your local computer, the image should be at http://localhost:3000/image.png.

背景画像を設定するために、相対パスURLをホストアドレスに割り振ることもできます。
以下のコードは、一例です。

You can then assign the URL relative to your host address to set the background image. Here's an example:

```
<div style={{ backgroundImage: "url(/image.png)" }}>
  Hello World
</div>
```

Setting the background image with relative URL

上記のサンプルコードのように、　/image.png に URL のパスを設定することで、ブラウザは、<your host address>/image.png で背景画像を探すことになります。

By setting the URL path to /image.png like the example above, the browser will look for the background image at <your host address>/image.png.

フォルダ内に、画像を配置したいならば、Public フォルダ内に別の画像用のフォルダを作成することもできます。

You can also create another folder inside public/ if you want to organize your images into folders. For example:

もしフォルダを新しく作成するならば、url(/img/image.png)を背景画像の値として、調整するのを忘れないようにしましょう。

Don't forget to adjust the backgroundImage value to url(/img/image.png) if you decide to create the folder.

絶対パスを使って、React 内に背景画像を設定する方法

### How to Set a Background Image in React Using the Absolute URL Method

あなたが、以下のコードのように React アプリの PUBLIC_URL の環境変数を使うことで、絶対パスURLを含めることもできます。

You can also include the absolute URL by using Create React App's PUBLIC_URL environment variable like this:

```
<div style={{
  backgroundImage: `url(${process.env.PUBLIC_URL + '/image.png'})`
}}>
  Hello World
</div>
```

Setting background image with absolute URL

あなたが、ローカル環境上で上記のコードを動かすとき、React スクリプトは、PUBLIC_URL の値をコントロールします。
ローカル環境で動かすとき、絶対パスのURLの代わりに、相対パス URLのように見えます。

When you run this on your local computer, React scripts will handle the value of the PUBLIC_URL value. When you run it locally, it will look like a relative URL instead of absolute URL:

absolute-url-background-image-1

画像の絶対パス URL は、ローカルコンピュータで表示されません。
Absolute URL of the image is not shown in local computer

あなたが、React を本番アプリケーションにデプロイしたとき、絶対パス URL は、表示されます。

The absolute URL will only be seen when you deploy React into production application later.



### How to Set a Background Image with Additional Properties
追加のプロパティと一緒に背景画像を設定する方法

If you want to customize the background image further, you can do so by adding additional properties after the backgroundImage. Here's an example:

もし、あなたが、さらに背景画像をカスタマイズしたいならば、the backgroundImageの後に、追加のプロパティを追加することで、カスタマイズできます。以下のコードは、そのサンプルです。

```
<div style={{
  backgroundImage: `url(${process.env.PUBLIC_URL + '/image.png'})`,
  backgroundRepeat: 'no-repeat',
  width:'250px'
}}>
  Hello World
</div>
```

Setting background-image with additional properties
<<<<<<< HEAD

追加のプロパティと一緒に、背景画像を設定する

The properties set above will add background-repeat: no-repeat and width: 250px together with the background-image style to the

element.
上記のコードのプロパティは、

要素に、background-repeat: no-repeat and width: 250px の CSS を追加しています。
Thank you for reading, and I hope you found this article useful. If you have any questions, you can find me on Twitter. I will share some short developer tips from time to time as well. 🙂

ここまでお読みいただき、ありがとうございます。そして、この記事が読者の皆様にとって、役に立っていることを願っています。 もし質問があるならば、Twitter 上で、私を見つけることができます。 今後も、短い開発者向けに役立つ情報も随時紹介していく予定です。
=======

追加のプロパティと一緒に、背景画像を設定する

The properties set above will add background-repeat: no-repeat and width: 250px together with the background-image style to the <div> element.

上記のコードのプロパティは、<div>要素に、background-repeat: no-repeat and width: 250pxのCSSを追加しています。

Thank you for reading, and I hope you found this article useful. If you have any questions, you can find me on Twitter. I will share some short developer tips from time to time as well. 🙂

ここまでお読みいただき、ありがとうございます。そして、この記事が読者の皆様にとって、役に立っていることを願っています。
もし質問があるならば、Twitter上で、私を見つけることができます。
今後も、短い開発者向けに役立つ情報も随時紹介していく予定です。
>>>>>>> a16b726e5fbbb6175fdb06199e611ccbc6173e6f
