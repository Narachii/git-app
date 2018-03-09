### React-native　入門編　　
![image](https://cdn-ak.f.st-hatena.com/images/fotolife/m/morugu/20170320/20170320094540.png)
   by Narachii
---

### React-nativeとは
Facebook社製のモバイルアプリ向けのフレームワーク

"learn once, write anywhere"の思想で作られており、  　
Android,iOSのアプリが簡単に作れる

---

Airbnbやskypeでも採用されています
![2018-03-07 20 41 13](https://user-images.githubusercontent.com/29746381/37192176-5303b30a-23a7-11e8-9616-d575745b688a.png)
http://facebook.github.io/react-native/showcase.html


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

---

#### フォルダ構成

- ios.js  (expo使用する場合は不要)
- Android.js   (expo使用する場合は不要)
- src (React Native)
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
---
###### npmのダウングレード(最新の5系は現在使えない！)
```
$ npm install -g npm@4.6.1
$ npm -v
  4.6.1
```
###### Watchmenのインストール
https://facebook.github.io/watchman/
```
$ brew install watchman
```

---

###### ReactNativeのインストール
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

#### Expoのインストール
- Expoとは？  
'Expo is a free and open source toolchain built around React Native to help you build native iOS and Android projects using JavaScript and React.'  
→　JS のみで ios/android アプリを作る開発/ビルド環境
https://expo.io/

---
#### サーバー立ち上げ
サーバー立ち上げは以下のコマンドで
```
npm start
```
---
#### Hello World
``` JS:App.js
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
今回はとりあえずHello Worldでしたが、
次回ではserverの構成なども含めて
話せるよう引き続き勉強しておきます！！！

---

### Thank you
