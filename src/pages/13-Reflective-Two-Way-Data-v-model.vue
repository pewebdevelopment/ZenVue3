<template>
    <div>
    <!-- <input type="text" v-model="name"> -->
    <Input v-model="name"/>
    </div>
</template>

<script>
import Input from '../components/13-Reflective-Two-Way-Data-v-model/input.vue'
export default {
    name: 'Reflective-Two-Way-Data-v-model',
    components: {
            Input,
    },
    data() {
        return {
            name:''
        }
            
    },
    methods: {}
        
        
    }
</script>

<style scoped>

</style>