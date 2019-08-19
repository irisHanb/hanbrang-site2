<template>
  <div class="experience">
    <ul class="items">
      <li class="item" v-for="(item, idx) in 5" :key="idx">
        <div class="header">
          <p class="title">(주)메가존</p>
          <div class="date">2019.08 ~ 2018.12</div>
        </div>
        <ul class="descs">
          <li class="desc">html, css, scss, css animation, javascript, vue</li>
        </ul>
      </li>
    </ul>
  </div>
</template>
<style lang="scss">
.experience {
  text-align: left;
  .header {
    padding-bottom: 0.5em;
    // display: flex;
    // justify-items: flex-start;
    // align-items: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.3);
    .title {
    }
    .date {
      opacity: 0.8;
      font-size: 0.9em;
    }
  }

  .item {
    margin-top: 1em;
  }

  .descs {
    margin-left: 1em;
    margin-top: 1em;
  }
}
</style>