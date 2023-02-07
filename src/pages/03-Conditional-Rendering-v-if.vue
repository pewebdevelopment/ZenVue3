<template>
    <div>
    <ConditionalRenderingVIf :num="40" display="true" showElement="true"/>
    </div>
</template>

<script>
import ConditionalRenderingVIf from '../components/03-Conditional-Rendering-v-if/Conditional-Rendering-v-if.vue';
    export default {
    name: '03-Conditional-Rendering-v-if',
    components: {
        ConditionalRenderingVIf,
    }
    }
</script>

<style scoped>

</style>