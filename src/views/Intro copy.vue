<template>
  <div class="intro">
    <ul class="list" v-for="(item, idx) in list" :key="idx">
      <li class="item">
        <p>{{item.date}}</p>
        <p class="texts">{{item.texts}}</p>
      </li>
    </ul>
  </div>
</template>
<script>
import { education } from "@/data/edu.js";
export default {
  data() {
    return {
      list: null
    };
  },
  created() {
    console.log("intro>>>", education);
    this.list = education;
  }
};
</script>
<style lang="scss">
.intro {
  // text-align: left;
  .item {
    margin-top: 2em;
    & > * {
      margin-top: 0.7em;
    }
  }
  .texts {
    font-size: 1.1rem;
    padding-left: 1.5em;
  }
}
</style>