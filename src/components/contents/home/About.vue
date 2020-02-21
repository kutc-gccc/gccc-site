<template>
  <section id="about">
    <h2>About</h2>
    <p>
      Game Creation Circle Cではゲームを作成する技術を学び、ハッカソンの開催、各種イベントへの展示などを行っています。
    </p>
    <h3>活動紹介</h3>
    <h4>講習</h4>
    <ul id="lecture-container">
      <li v-for="lectureData in lectureDataList" :key="lectureData.name" class="lecture-box">
        <h3>{{ lectureData.name }}</h3>
        <i v-if="lectureData.iconClass" :class="lectureData.iconClass"/>
        <img v-if="lectureData.iconPath" :src="lectureData.iconPath"/>
        <p>{{ lectureData.description }}</p>
      </li>
    </ul>
    <h4>イベント</h4>
    <h5>ハッカソン</h5>
    <p>
      現在ハッカソンの開催を予定しています詳細が決まり次第、Newsに追加していきます!
    </p>
    <h5>夏コミ</h5>
    <p>
      夏コミの参加申請を行いました。夏コミに向けてゲーム開発を続けています。
    </p>
    <h5>情祭</h5>
    <p>
      総合情報学部で開催される学祭にゲームを展示します。
    </p>
    <h4>その他</h4>
    <h5>いろんなゲーム機</h5>
    <p>家庭用機ならFCからSwitchまで、PSからPS4まで取り揃えております！</p>
  </section>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

interface LectureData {
  name: string;
  iconClass?: string;
  iconPath?: string;
  imgPath: string;
  description: string;
  descriptionDetail: string;
}

@Component
export default class About extends Vue {
  private lectureDataList: LectureData[] = [];

  public created() {
    this._storeLectureData();
    console.log(this.lectureDataList);
  }

  private _storeLectureData() {
    this.lectureDataList.push({
      name: "プログラミング講習",
      iconClass: "fas fa-laptop-code fa-6x",
      imgPath: "",
      description: "ロジックを考える基礎となるプログラミングの能力を教えます！",
      descriptionDetail: "ゲームエンジンを持ってしても、基本的なプログラミング能力は必要になります。\
      そのためにC言語を用いてプログラミングの基本的な技術を学びます！",
    });
    this.lectureDataList.push({
      name: "グラフィック講習",
      iconClass: "fas fa-cube fa-6x",
      imgPath: "",
      description: "2D絵を書く基本となる技術や、Mayaを用いた3Dモデリングの手法を教えます！",
      descriptionDetail: "前半では人間の顔や体の書き方を初め、講習を受ける人達の要望に答えた内容の講習を行います。\
      後半はMayaを用いた3Dモデリングやアニメーション、ゲームへの統合の仕方など、より実践的な技術を教えます",
    });
    this.lectureDataList.push({
      name: "音楽講習",
      iconClass: "fas fa-music fa-6x",
      imgPath: "",
      description: "作曲のためのFLStudioの使い方からはじめ、音楽理論なども教えます！",
      descriptionDetail: "作曲するためのDTMであるFLStudioの使い方を学び、音楽理論、コード進行などの基礎を抑えます。\
      その後ミックスなど実際に曲を作るフロー全体を学び、BGMを作曲するまでの技術を教えます。",
    });
    this.lectureDataList.push({
      name: "企画講習",
      iconClass: "fas fa-book-open fa-6x",
      imgPath: "",
      description: "どのようにゲームを企画し、開発を進めていくのかを教えます！",
      descriptionDetail: "仮",
    });
    this.lectureDataList.push({
      name: "Unity講習",
      iconPath: require("@/assets/img/logos/unity.png"),
      imgPath: "@/assets/img/logos/unity.png",
      description: "Unityを用いたゲーム作成の基礎を教えます！",
      descriptionDetail: "Unityを用いたゲーム作成の基礎を教えます！",
    });
  }
}
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
    padding: 0;
    transition-duration: 1s;

    .lecture-box {
      flex-direction: column;
      justify-content: center;
      align-items: center;
      list-style: none;
      border: thin solid #000;
      border-radius: 16px;
      margin: 1vw;
      padding: 2vh;

      // responsive for smartphone
      @media screen and (max-width: 480px) {
        width: 80%;
      }
      width: 40%;
      height: 250px;
      h3 {
        font-size: 2vw;
        margin: 0.5vh 0;
      }
      img {
        height: 45%;
        padding-right: 10%;
      }
      i {
        margin: 1vh;
      }
    }
  }
}
</style>