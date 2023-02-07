<template>
    <div>
<ClickCounter/>
<HoverCounter/>
    </div>
</template>

<script>
import ClickCounter from '../components/31-Composition-API-Ref-Reactive-Reusability/ClickCounter.vue'

import HoverCounter from '../components/31-Composition-API-Ref-Reactive-Reusability/HoverCounter.vue'

export default {
    name: '31-Compositon-API-Ref-Reactive-Reusability',
        components: {
            ClickCounter,
            HoverCounter,
        }
        
    }
</script>

<style scoped>

</style>