<template>
  <CoronaData msg="코로나 확진자 데이터" />
</template>


<script>
import CoronaDataVue from "./components/CoronaData.vue";
export default {
  name: "App",
  components: {
    CoronaData: CoronaDataVue,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
