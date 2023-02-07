<template>
                    <div>
<button class="btn" @click="incrementCount">Clicked {{ count }} times</button>
                    </div>
</template>

<script>
import CounterMixins from '../mixins/counter'
                    export default {
                    name: 'clickCounter',
                    mixins:[CounterMixins],
                   
                    }
</script>

<style scoped>

</style>