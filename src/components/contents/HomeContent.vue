<template>
  <section id="home-content">
    <section class="top-content">
      <Introduction/>
    </section>
    <section class="bottom-content">
      <section class="left-container">
        <About/>
        <News/>
      </section>
      <section class="right-container">
        <TwitterBar twitterId="GCCCinfo" profile="profile" tweetLimit=5></TwitterBar>
      </section>
    </section>
  </section>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

import Introduction from "./home/Introduction.vue";
import About from "./home/About.vue";
import News from "./home/News.vue";
import TwitterBar from "./home/TwitterBar.vue";

@Component({
  components: {
    Introduction,
    About,
    News,
    TwitterBar,
  },
})
export default class HomeContent extends Vue {}
</script>

<style scoped lang="scss">
#home-content {
  display: flex;
  flex-direction: column;
  transition-duration: 0.5s;
  .top-content {
    height: 100%;
  }

  .bottom-content {
    margin: 2vh 4vw;
    display: flex;
    flex-direction: row;
    .left-container {
      display: flex;
      flex-direction: column;
    }
    @media screen and (max-width: 600px) {
      .right-container {
        display: none;
      }
    }
    .right-container {
      border-left: solid thin #ddd;
      width: 30vw;
      padding: 0 8px;
    }
  }
}
</style>

<style lang="scss">
// bottom container heading css. affect About.vue and News.vue
h2 {
  margin-top: 0;
  padding: 0 2vw;
  font-size: 5vh;
  border-bottom: medium solid #000;
}
h3 {
  margin: 1vh 0;
  font-size: 4vh;
}
h4 {
  margin: 0.8vh 0;
  font-size: 3.5vh;
}
p {
  margin: 0.5vh 0;
}
</style>
