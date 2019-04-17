<template>
   <li @click="onItemSelect">
        {{toDoTasks}}
    </li>
</template>

<script>

export default {
    name: 'ListItem',
    props: {
        toDoTasks: Array
    },
    methods: {
        onItemSelect() {
            return alert("clicked!")
        }
    }
}
</script>

