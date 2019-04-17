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
            this.$emit('removeTask', this.toDoTask)
        }
    }
}
</script>

