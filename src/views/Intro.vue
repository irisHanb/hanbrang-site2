<template>
  <div class="intro">
    <List title="자격 사항" :list="certificationsData" />
    <List title="학력 사항" :list="eduData" />
  </div>
</template>
<script>
import List from "@/components/List.vue";
import education from "@/data/edu.js";
import certifications from "@/data/certifications.js";
import { constants } from "crypto";
export default {
  components: { List },
  data() {
    return {
      eduData: null,
      certificationsData: null
    };
  },
  created() {
    this.eduData = education;
    this.certificationsData = certifications;
    console.log(this.eduData);
  }
};
</script>
<style lang="scss">
.intro {
  text-align: left;
}
</style>