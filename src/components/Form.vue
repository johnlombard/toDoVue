<template>
    <div>
        <h1>Form</h1>
        <input @input="onInput"/>
    </div>
</template>

<script>
export default {
    name: 'Form',
    methods: {
        onInput(event) {
            this.$emit('termChange', event.target.value)
        }
    }
};
</script>
