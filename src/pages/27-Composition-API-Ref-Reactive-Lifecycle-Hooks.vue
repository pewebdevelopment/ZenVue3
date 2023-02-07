<template>
    <div>
        <LifecycleC/>
        <LifecycleO/>
    </div>
</template>

<script>
import LifecycleC from '../components/27-Composition-API-Ref-Reactive-Lifecycle-Hooks/LIfecycleC.vue'

import LifecycleO from '../components/27-Composition-API-Ref-Reactive-Lifecycle-Hooks/LIfecycleO.vue'
export default {
    components: {
            LifecycleC,
            LifecycleO,
        }
        
    }
</script>

<style scoped>

</style>