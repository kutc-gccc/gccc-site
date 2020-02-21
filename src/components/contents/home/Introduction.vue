<template>
  <section class="bg">
    <section id="introduction">
      <h1>
        <span class="head-emphasis">G</span>ame<br>
        <span class="head-emphasis">C</span>reaction<br>
        <span class="head-emphasis">C</span>ircle<br>
        <span class="head-emphasis">C</span>
      </h1>
      <p class="catch-copy">ゲーム、作ろう！</p>
      <p class="techs">Unity / FLStudio / Maya / Siv3D</p>
      <Button linkHref="https://twitter.com/gcccinfo" snsType="Twitter"/>
    </section>
  </section>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import Button from "@/components/parts/Button.vue";

@Component({
  components: {
    Button,
  },
})
export default class Introduction extends Vue {}

</script>

<style lang="scss" scoped>
.bg {
  background-image: url("../../../assets/img/bgs/top-background.jpg");
  background-size: cover;
}

#introduction {
  background-color: rgba(0,0,0,0.45);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  height: 80vh;
  width: 100%;
  transition: all 0.5s ease;
  h1 {
    color: #eef;
    font-size: 8vh;
    padding: 0;
    margin: 0;
    margin-top: 20px;
    text-align: left;
    line-height: 1em;
    transition: all 0.5 ease;
  }
  .head-emphasis {
    color: rgb(141, 219, 77);
  }
  .catch-copy {
    color: #eff;
    font-size: 5vh;

  }
  .techs {
    margin: 0;
    padding: 0;
    color: #eee;
    font-size: 2.5vh;
  }
}

</style>