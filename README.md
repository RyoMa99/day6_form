# day6
[vue form 色々](https://reffect.co.jp/vue/vue-js-input-operate#i-9)

## 学んだこと
- チェックボックスは真偽値以外もデータを持たせられる。
  ```js
  <input
    v-model="checkValue"
    type="checkbox"
    true-value="はい"
    false-value="いいえ"
  >
  ```
- 配列にvalueが存在するかどうかの真偽値で判断することも出来る
  ```js
  <input
    v-model="checkValues"
    type="checkbox"
    value="ラグビー"
  > ラグビー
  <input
    v-model="checkValues"
    type="checkbox"
    value="サッカー"
  > サッカー
  <input
    v-model="checkValues"
    type="checkbox"
    value="バスケットボール"
  > バスケットボール
  ```
- セレクトボックスはdisabledを使ってプレースホルダーの様な役割を与えられる
  ```js
  <option
    disabled
    value=""
  >
    興味のあるスポーツを選択
  </option>
  ```
- Event型はinterfaceでtargetがない。`event.target instanceof HTMLInputElement`を用いて型ガードを通す必要がある。
  (参考)[https://yuutookun.hatenablog.com/entry/2018/07/21/084912]

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Run your unit tests
```
yarn test:unit
```

### Run your end-to-end tests
```
yarn test:e2e
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
