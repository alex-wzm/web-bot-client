<template>
  <div>
    <div class="footer">
      <github-button
        href="https://github.com/alex-wzm/vue-web-bot"
        data-icon="octicon-star"
        data-size="large"
        aria-label="Star alex-wzm/vue-web-bot on GitHub"
      >Star</github-button>
      <p>v{{ currentVersion }}</p>
      <a href="https://vuejs.org/" target="_blank">
        <img height="50px" alt="Vue logo" src="../assets/logo.png" />
      </a>
    </div>
  </div>
</template>

<script>
import GithubButton from "vue-github-button";
export default {
  name: "AppFooter",
  components: { GithubButton },
  data() {
    return {
      currentVersion: process.env.VUE_APP_VERSION
    };
  }
};
</script>

<style scoped>
.footer {
  position: fixed;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  left: 0;
  bottom: 0;
  width: 100%;
  background: rgb(255, 255, 255);
  background: linear-gradient(
    0deg,
    rgba(255, 255, 255, 1) 0%,
    rgba(255, 255, 255, 0.66) 66%,
    rgba(255, 255, 255, 0) 100%
  );
}
.footer > * {
  margin: 0.5% 1%;
}
</style>