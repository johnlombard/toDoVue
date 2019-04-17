<template>
   <li>
        {{toDoTask}}
        <button @click="onDelete">X</button>
    </li>
</template>

<script>

export default {
    name: 'ListItem',
    props:['toDoTask'],
    methods: {
        onDelete(){
            console.log("clicked")
        }
    }
}
</script>

