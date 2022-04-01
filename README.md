# HTML5のWeb Audio API(AudioContext)を使ってみる

## Web Audio APIとは

ブラウザ上で複雑で動的な音声操作を実現できるようにしたAPI
(立体音響を制御することもできるらしい)
[Web Audio API \- Web API \| MDN](https://developer.mozilla.org/ja/docs/Web/API/Web_Audio_API)

## 対応ブラウザ

IE以外のブラウザで対応
[Web Audio API \| Can I use\.\.\. Support tables for HTML5, CSS3, etc](https://caniuse.com/audio-api)

## 音とは

音とは`振動`である

- 音の大きさは振幅で決まる。
  - 振幅が大きいと音も大きい
  - 振幅が小さいと音も小さい
- 音の高さは周波数（一秒間に空気が振動する回数）で決まる。
  - 振動数が多いと高い音になる
  - 振動数が少ないと低い音になる

[音階](https://hochouki.soudan-anshin.com/cont/sound/)

## 使い方

簡潔で通常の Web Audio の使い方は次のようになります:

1. オーディオコンテキストを作成する
1. コンテキストの中で、<audio>,オシレーター,ストリームなどの音源を作成する
1. リバーブ・フィルター・パンナー・コンプレッサーなどのエフェクトノードを作成する
1. 最終的な音声の到達先を選ぶ(例えばスピーカー)
1. 音源をエフェクトに繋げ、エフェクトを到達先(destination)に繋げる

なるほどわからん！！！オーディオインターフェースとか分かる人はすんな理解できるんかな？


## 実装してみた

注意: ユーザー始動じゃないと発火しないようになっている

```
The AudioContext was not allowed to start. It must be resumed (or created) after a user gesture on the page
```

## 実行方法

HTTPサーバーを起動

```
$ python3 -m http.server
```

`http://localhost:8000`をブラウザで開く

## こんな使い方ありかも

- フォーム送信時のバリデーションエラー、成功で音を出し分ける。

## 参考

[【HTML5】マリオのコインの音をブラウザで出そう【ファミコン】 \- Qiita](https://qiita.com/kurokky/items/f18341c17ad846332569)
