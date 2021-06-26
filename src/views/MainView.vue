<template>
  <div>
    <p>{{ textInput }}</p>
    <!-- テキスト -->
    <input
      v-model="textInput"
      type="text"
    >
    <!-- テキストエリア -->
    <textarea v-model="textInput" />
    <p>{{ checkValue }}</p>
    <!-- 真偽値以外のチェックボックス -->
    <input
      v-model="checkValue"
      type="checkbox"
      true-value="はい"
      false-value="いいえ"
    >
    <!-- チェックボックス配列 -->
    <p>{{ checkValues }}</p>
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
    <!-- ラジオボタン -->
    <p>{{ radioValue }}</p>
    <input
      v-model="radioValue"
      type="radio"
      value="ラグビー"
    > ラグビー
    <input
      v-model="radioValue"
      type="radio"
      value="サッカー"
    > サッカー
    <input
      v-model="radioValue"
      type="radio"
      value="バスケットボール"
    > バスケットボール
    <!-- セレクトボックス -->
    <p>{{ selectValue }}</p>
    <select v-model="selectValue">
      <option
        disabled
        value=""
      >
        興味のあるスポーツを選択
      </option>
      <option>値1</option>
      <option>値2</option>
      <option>値3</option>
    </select>
    <!-- セレクトボックス 複数 -->
    <p>{{ selectValues }}</p>
    <select
      v-model="selectValues"
      multiple=""
    >
      <option
        disabled
        value=""
      >
        興味のあるスポーツを選択
      </option>
      <option>値1</option>
      <option>値2</option>
      <option>値3</option>
    </select>
    <!-- ファイルオブジェクト -->
    <p>{{ fileData.name }}</p>
    <input
      type="file"
      @change="handleFile"
    >
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component({})
export default class extends Vue {
  textInput = ''
  checkValue = 'いいえ'
  checkValues = []
  radioValue = ''
  selectValue = ''
  selectValues = []
  fileData = new File([], '')

  handleFile (event: InputEvent): void {
    if (!(event.target instanceof HTMLInputElement)) return
    if (event.target.files === null) return
    const file = event.target.files[0]
    this.fileData = file
  }
}
</script>

<style lang="scss" scoped>

</style>
