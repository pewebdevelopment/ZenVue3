<template>
    <div>
<button class="btn" @click="activeTab='TabA'">TabA</button>
<button class="btn" @click="activeTab='TabB'">TabB</button>
<button class="btn" @click="activeTab='TabC'">TabC</button>

<keep-alive>
<component :is="activeTab"/>
</keep-alive>

<!-- <TabA v-if="activeTab==='TabA'"/>
<TabB v-if="activeTab==='TabB'"/>
<TabC v-if="activeTab==='TabC'"/> -->
    </div>
</template>

<script>
import TabA from '../components/16-Dynamic-Components-and-Keep-Alive/TabA.vue'
import TabB from '../components/16-Dynamic-Components-and-Keep-Alive/TabB.vue'
import TabC from '../components/16-Dynamic-Components-and-Keep-Alive/TabC.vue'
export default {
    name: '16-Dynamic-Components-and-Keep-Alive', 
    data() {
        return{
            activeTab: 'TabA',
        }
    },
    components: {
        TabA,
        TabB,
        TabC,
    }
        
    }
</script>

<style scoped>

</style>