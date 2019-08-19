<template>
  <div class="list-wrap">
    <h3 class="title">{{title}}</h3>
    <ul class="list">
      <li class="item" v-for="(item, idx) in list" :key="idx">
        <div class="date">{{item.date}}</div>
        <div class="texts">{{item.texts}}</div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: ["title", "list"],
  data() {
    return {};
  },
  created() {
    console.log(this.data);
  }
};
</script>
<style lang="scss">
.list-wrap {
  .title {
    margin-top: 2em;
    padding-bottom: 0.3em;
    font-weight: bold;
    font-size: 1.3rem;
    border-bottom: 1px solid rgba(255, 255, 255, 0.3);
    text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.3);
  }
  .list {
    padding-left: 1.3em;
  }
  .item {
    display: flex;
    justify-content: flex-start;
    margin-top: 1em;
  }
  .texts {
    font-weight: 700;
    margin-left: 0.7em;
  }
}
</style>