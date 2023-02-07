<template>
    <div>
        <h4>App Component</h4>
        <!-- <ChildStyles/> -->
        <ChildStyles>
            <h4>Child Style Component</h4>
        </ChildStyles>

    </div>
</template>

<script>
import ChildStyles from '../components/15-Component-Styles/ChildStyles.vue'
export default {
    name: '15-Component-Styles',
    components: {
        ChildStyles,
    }
        
    }
</script>

<style scoped>
h4{color:orange;
}
</style>