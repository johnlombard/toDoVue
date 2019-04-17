<template>
    <div>
        <h1>Form</h1>
        <input @input="onInput"/>
        <button @click="onClick">Add to list</button>
    </div>
</template>

<script>
export default {
    name: 'Form',
    methods: {
        onClick(event) {
            this.$emit('addTask', event.target.value)
        },
        onInput(event) {
            this.$emit('termChange', event.target.value)
        }
    }
};
</script>
