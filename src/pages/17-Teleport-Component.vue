<template>
    
        <teleport to="#portal-root">
        <Portal/>
        </teleport>
   
</template>

<script>
import Portal from '../components/17-Teleport-Component/portal.vue'
    export default {
    name: '17-Teleport-Component',
    components: {
        Portal,
    }
        
    }
</script>

<style scoped>

</style>