<template>
    <ul>
        <ListItem
        v-for="(toDoTask, index) in toDoTasks"
        :toDoTask="toDoTask"
        :key="`toDoTask-${index}`"
       @removeTask="onDelete"
        ></ListItem>
    </ul>
</template>

<script>
import ListItem from './ListItem';

export default {
    name: 'List',
    components: {
        ListItem
    },
    props: {
        toDoTasks: Array
    },
    methods: {
        onDelete(toDoTask){
this.toDoTasks.splice(this.toDoTasks.indexOf(toDoTask), 1)   
console.log(`Tasks + ${this.toDoTasks}`)
 }
    }

}
</script>

<style scoped>
ul{
   list-style: none;
}
li {
    cursor: pointer;
}

li:hover {
    background-color: #eeeeee
}
</style>

