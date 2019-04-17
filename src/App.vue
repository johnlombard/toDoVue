<template>
  <div id="app">
    <Header></Header>
    <Form @termChange="onTermChange" @addTask="addTask"></Form>
    <List :toDoTasks="toDoTasks"></List>
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
    return {
      userEntry: '', 
      toDoTasks: []}
  },
  methods: {
    addTask(){
      this.toDoTasks.push(this.userEntry)
    },
    
    onTermChange(task) {
      this.userEntry = task
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