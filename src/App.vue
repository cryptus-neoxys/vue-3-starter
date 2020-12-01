<template>
  <button v-on:click="setShow">Hello</button>
  <h1>
    {{ title }} from
    <h1 v-html="showName"></h1>
  </h1>
  <input v-model="name" type="text" v-on:input="setName" />
</template>

<script>
export default {
  data() {
    return {
      title: "Heyy Vueee3",
      name: "Dev Sharma",
      showName: "Dev Sharma",
    };
  },
  methods: {
    setShow() {
      this.showName = this.showName
        .split("")
        .reverse()
        .join("");
    },
    setName() {
      this.showName = this.name;
    },
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
