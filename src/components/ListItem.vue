<template>
   <li @click="onItemSelect">
       <div>
           <!-- {{task}} -->
       </div>
    </li>
</template>

<script>

export default {
    name: 'ListItem',
    methods: {
        onItemSelect() {
            return alert("clicked!")
        }
    }
}
</script>

