<template>
  <div class="survay">
    <h1>Страница - "{{ title }}"</h1>
    <NuxtLink class="survey__link" to="/survey/create-survey">Добавить опрос</NuxtLink>
  </div>
</template>

<script>
export default {
  name: "Survay",

  data() {
    return {
      title: "",
    };
  },

  mounted() {
    this.$store.commit("setCurrentRootPageName", this.$route.path);
    this.title = this.$store.getters.currentRootPageName;
  },
};
</script>

<style scoped>
.survey__link {
  color: rgba(4, 0, 255, 0.75);
  outline: none;
  text-decoration: none;
  font-size: 15px;
  line-height: 1.6;
}
</style>
