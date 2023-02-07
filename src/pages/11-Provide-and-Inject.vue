<template>
    <div>
   <ComponentC/>
   <h3>App component username {{ name }}</h3>
    </div>
</template>

<script>
import ComponentC from '../components/11-Provide-and-Inject/ComponentC.vue'
export default {
    name:'11-Provide-and-Inject',
    components: {
            ComponentC,
    },
    data() {
        return {
            name: 'Vishwas',
            
            }
    },
    provide() {
        return {
            username: this.name,
        }
        
    },
    }
</script>

<style scoped>

</style>