<template>
                    <div>
<clickCounter/>
<hoverCounter/>
                    </div>
</template>

<script>
import clickCounter from './clickCounter.vue'
import hoverCounter from './hoverCounter.vue'
                    export default {
                    name: 'Reusability-via-mixins-and-composables',
                    components: {
                                        clickCounter,
                                        hoverCounter,
                    }                    
                    }
</script>

<style scoped>

</style>