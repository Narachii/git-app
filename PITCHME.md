### React-native by Narachii

---

### React-nativeとは
Facebook製のモバイルアプリ向けのフレームワーク

---

### Airbnbやskypeでも採用されています
http://facebook.github.io/react-native/showcase.html



![Video](https://www.youtube.com/embed/mkiDkkdGGAQ)

---

#### なぜReact-native？
 - ios・Androidの双方でデプロイが可能
   (learn once, write anywhere!!!)

 - JSをコア言語としており、Webライクな開発スタイルである！
    (Swift・Javaの勉強いらない?!)
 
 - サーバサイドはFirebaseがおすすめみたいです
    https://firebase.google.com/

---

#### デメリット
 - 日本語の文献がまだほとんどない

 - Componentを自作 or 外部moduleの拡張する場合は、iOS, Androidの知識が必要

 - Reactの理解が必要
  (JSX,props,state, Redux)

---
####　サーバー構成？
Expoとか

---

#### フォルダ構成
src (React Native)
- actions (http通信周り)
- components (部品レベル)
- containers (ページレベル/reduxとconnectする部分)
- reducers (actionを受けてstateを変更するめそd)
- store (アプリケーションの状態を保持する)

---

#### Sample Code
```
import React, { Component } from 'react';
import { AppRegistry, Text, View } from 'react-native';

class Blink extends Component {
  constructor(props) {
    super(props);
    this.state = {isShowingText: true};

    // Toggle the state every second
    setInterval(() => {
      this.setState(previousState => {
        return { isShowingText: !previousState.isShowingText };
      });
    }, 1000);
  }

  render() {
    let display = this.state.isShowingText ? this.props.text : ' ';
    return (
      <Text>{display}</Text>
    );
  }
}

export default class BlinkApp extends Component {
  render() {
    return (
      <View>
        <Blink text='I love to blink' />
        <Blink text='Yes blinking is so great' />
        <Blink text='Why did they ever take this out of HTML' />
        <Blink text='Look at me look at me look at me' />
      </View>
    );
  }
}
```

---
### Hello World しちゃおう！！！
```
$brew install node

nodebrewのinstall
$ curl -L git.io/nodebrew | perl - setup
$ vi .bashrc
  export PATH=$HOME/.nodebrew/current/bin:$PATH
$ source .bashrc
$ echo $PATH
$ nodebrew help
  nodebrew 0.9.7
$ nodebrew ls-remote
$ nodebrew install-binary vX.X.X
$ nodebrew ls
  vX.X.X
  current: none
$ nodebrew use vX.X.X
sudo npm install -g create-react-app

```
npmのダウングレード(最新の5系は現在使えない！)
```
$ npm install -g npm@4.6.1
$ npm -v
  4.6.1
```
Watchmenのインストール
https://facebook.github.io/watchman/
```
$ brew install watchman
```
ReactNativeのインストール
```
$ npm install -g create-react-native-app
```

---
#### React appの作成！
```
$ create-react-native-app AwesomeProject
$ cd AwesomeProject
```
---

#### Expoをインストール
- Expoとは？
(Expoの写真)

---
#### サーバー立ち上げ
サーバー立ち上げは以下のコマンドで
```
npm start
```
---
#### Hello World
```
vim App.js
```
以下に編集
```
import React, { Component } from 'react';
import { Text } from 'react-native';

export default class HelloWorldApp extends Component {
  render() {
    return (
      <Text>Hello world!</Text>
    );
  }
}
```

---

#### 最後に

---

```
body {
  backgroundcolor: #fff;
  color: #333;
  font-family: verdana, arial, helvetica, sans-serif;
  font-size: 13px;
  line-height: 18px;
}
```
@[2](なんかちゃうで)
---

### Thank you
