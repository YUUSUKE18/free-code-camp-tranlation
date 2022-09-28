![元記事](https://www.freecodecamp.org/news/react-background-image-tutorial-how-to-set-backgroundimage-with-inline-css-style/)

## React Background Image Tutorial – How to Set backgroundImage with Inline CSS Style

##

React のインライン CSS にて使える backgroundImage スタイルプロパティを設定するには、4 つの方法があります。

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

上のコードは、<background-image: url(https://via.placeholder.com/500)>のスタイルが適用された一つの<div>要素として、描画をします。

### How to Set a Background Image in React From Your /src Folder

### ご自身の/src フォルダ配下から React での背景画像の設定方法

React を使い、アプリケーションを開発する、そして、src/フォルダ内部の画像を持っているならば、最初に画像を取り込み、要素の背景として、配置します。

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
取り込んだ画像を用いて、画像として設定する方法

npm start コマンドにて、アプリケーションを起動するとき、画像が見つけられないとして、React アプリケーションは、コンパイルに失敗したというエラーを表示し、ビルドを停止します。

この方法だと、アプリケーション上で、いかなる画像リンクも表示されません。上のコードにおいて、<backgroundImage>の値は、開発者が JavaScript 表記にて埋め込めるテンプレート文字を使っています。
