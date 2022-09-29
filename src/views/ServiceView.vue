<template>
  <div>
    <template-view>
      <div class="container">
        <h1>This is my ServiceView Page</h1>
        <!-- <p v-for="(a,project) in 10" :key="project">This is a Vue.js project.</p> -->
        <p v-if="flag == true">
          <img src="../assets/lighton.jpg" alt="" />
        </p>
        <p v-else>
          <img src="@/assets/lightoff.jpg" alt="" srcset="" />
        </p>
        <button @click="setflag()">Set</button>
      </div>
    </template-view>
  </div>
</template>

<script>
import TemplateView from "./TemplateView.vue";

export default {
  components: { TemplateView },
  name: "ServiceView",

  data() {
    return {
      flag: false,
    };
  },

  methods: {
    setflag() {
      this.flag = !this.flag;
    },
  },
};
</script>

<style scoped>
</style>