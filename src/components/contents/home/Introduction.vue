<template>
  <section class="bg">
    <section id="introduction">
      <h1>
        <span class="head-enphasis">G</span>ame<br>
        Creation<br>
        Circle<br>
        C
      </h1>
      <p>Unity / UnrealEngine / Siv3D / DxLib / Tyrano Builder</p>
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
  background-image: url("/img/top-background.jpg");
  background-size: cover;
}

#introduction {
  background-color: rgba(0,0,0,0.45);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  height: 80vh;
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
  .head-enphasis {
    color: #5ee;
  }
  p {
    margin: 0;
    padding: 0;
    color: #eee;
    font-size: 24px;
  }
}

</style>