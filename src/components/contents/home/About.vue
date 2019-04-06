<template>
  <section id="about">
    <h2>About</h2>
    <p>
      Game Creation Circle Cではゲームを作成する技術を学び、ハッカソンの開催、各種イベントへの展示などを行っています。
    </p>
    <h3>活動紹介</h3>
    <h4>講習</h4>
    <section id="lecture-container">
      <section class="lecture-box">
        
        <img src="" alt="">
        <p>ロジックを考える基礎となるプログラミングの能力を教えます！</p>
      </section>
      <section class="lecture-box">
        <img src="" alt="">
        <p>イラストや3DCGのモデリングの方法やゲームへの統合方法を教えます！</p>
      </section>
      <section class="lecture-box">
        <img src="" alt="">
        <p>DTMを用いた作曲や音楽理論の基礎を教えます！</p>
      </section>
      <section class="lecture-box">
        <img src="" alt="">
        <p>ゲームのプロダクションに関わる能力を教えます！</p>
      </section>
      <section class="lecture-box">
        <img src="" alt="">
        <p>Unityを用いたゲーム作成の基礎を教えます！</p>
      </section>
    </section>
    <h4>イベント</h4>
    <h5>夏コミ</h5>
      <p>夏コミの参加申請を行いました。夏コミに向けて様々なゲームを開発しています。
    <h5>情祭</h5>
      <p>総合情報学部で開催される学祭にゲームを展示します。</p>
    <h4>その他</h4>
    <h5>スマブラ</h5>
    <p>腕に自身がある方も！初心者でも！履修相談しながら楽しくスマブラ！</p>
  </section>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class About extends Vue {}
</script>

<style lang="scss" scope>
#about {
  border-bottom: solid thin gray;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 1vh;
  // heading query css on HomeContent.vue

  #lecture-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    .lecture-box {
      border: thin solid #000;
      margin: 1vw;
      height: 240px;
      width: 300px;
    }
  }
}
</style>