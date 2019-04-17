<template>
  <div id="app">
    <Header></Header>
    <Form @termChange="onTermChange"></Form>
    <List></List>
    {{tasks}}
  </div>
</template>

<script>
import List from "./components/List.vue";
import Header from "./components/Header.vue";
import Form from "./components/Form.vue";

export default {
  name: "app",
  components: {
    Header,
    List,
    Form
  },
  data() {
    return {tasks: ["do yo shit"]}
  },
  methods: {
    onTermChange(task) {
      this.tasks = task
    }
  }
};
</script>

<style>
html {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: rgb(95, 183, 131);
  background-color: rgb(56, 73, 94);
  text-align: center;
}
/* #app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: rgb(95, 183, 131);
  background-color: rgb(56, 73, 94);
  text-align: center;
} */
</style>