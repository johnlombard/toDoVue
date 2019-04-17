<template>
    <ul>
        <ListItem></ListItem>
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
    }

}
</script>

