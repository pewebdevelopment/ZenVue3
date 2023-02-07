<template>
    <div>
        
        <Data />
        <DemoOne/>
        <DemoTwo/>
    </div>
</template>

<script>
import Data from '../components/22-Composition-API-Ref-reactive-Tokens/Data.vue'

import DemoOne from '../components/22-Composition-API-Ref-reactive-Tokens/DemoOne.vue'

import DemoTwo from '../components/22-Composition-API-Ref-reactive-Tokens/DemoTwo.vue'
export default {
    name: '22-Composition-API-Ref-reactive-Tokens',
    components: {
        Data,
        DemoOne,
        DemoTwo,
    }
        
        
    }
</script>

<style scoped>

</style>