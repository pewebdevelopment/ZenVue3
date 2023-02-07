<template>
    <div>
    <Binding greet="Hello" name="Batman" channel="codevolution" channel2="<b>Codevolution2</b>" />
    </div>
</template>

<script>
import Binding from '../components/02-Binding-v-bind/Binding-v-bind.vue';
export default {
    name: '02-Binding-v-bind',
    components: {
        Binding,
    }

}
</script>

<style lang="scss" scoped>

</style>