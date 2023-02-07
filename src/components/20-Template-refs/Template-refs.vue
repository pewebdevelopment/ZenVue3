<template>
                    <div>
                    <input type="text" ref="inputRef"/>
                    <PostList ref="postListRef"/>
                    </div>
</template>

<script>
import PostList from '../18-HTTP-and-Components/PostList.vue'
                    export default {
                    name: 'Template-refs',
                    components: {
                                        PostList,
                    },
                    mounted() {
                                        console.log(this.$refs.postListRef)

                                        this.$refs.inputRef.focus()
                                        },
                    }
</script>

<style scoped>

</style>