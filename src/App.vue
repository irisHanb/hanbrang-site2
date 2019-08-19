<template>
  <div id="app" :style="{backgroundColor: bgColor}">
    <div class="wrap">
      <ul id="nav">
        <li>
          <router-link to="/">Intro</router-link>
        </li>
        <li>
          <router-link to="/experience">Work Experience</router-link>
        </li>
        <li>
          <router-link to="/portfolio">Portfolio</router-link>
        </li>
      </ul>
      <div class="page">
        <transition name="fade" mode="out-in">
          <router-view />
        </transition>
      </div>
    </div>
  </div>
</template>
<script>
const BG_DEFUALT = "#e67700";
export default {
  data() {
    return {
      sectionName: "about"
    };
  },
  created() {
    this.sectionName = this.$route.name;
  },
  updated() {
    // console.log(this.$route);
    this.sectionName = this.$route.name;
  },
  methods: {},
  computed: {
    bgColor() {
      switch (this.sectionName) {
        case "about":
          return BG_DEFUALT;
        case "experience":
          return "#C2255C";
        case "portfolio":
          return "#1864AB";
        default:
          return BG_DEFUALT;
      }
    }
  },
  watch: {}
};
</script>

<style lang="scss">
#app {
  min-height: 100vh;
  transition: all 0.7s ease-in-out;
}
.wrap {
  max-width: 500px;
  padding: 60px 10px 30px 10px;
  margin: 0 auto;
}
#nav {
  padding: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  li {
    &:nth-child(2) {
      // margin: 0 1em;
      &:before,
      &:after {
        content: "|";
        color: rgba(255, 255, 255, 0.7);
        margin: 0 1.3em;
      }
    }
  }
  a {
    font-weight: bold;
    color: #fff;
    text-decoration: none;
    border-bottom: 1px solid transparent;
    transition: all 0.5s ease-in-out;

    &.router-link-exact-active {
      color: #fff;
      text-shadow: 3px 3px 5px #000000;
    }
  }
}
</style>
