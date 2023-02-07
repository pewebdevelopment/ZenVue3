<template>
    <div>
<PostList/>
<CreatePost/>
    </div>
</template>

<script>
import PostList from '../components/18-HTTP-and-Components/PostList.vue'

import CreatePost from '../components/18-HTTP-and-Components/createPost.vue'
export default {
    name: '18-HTTP-and-Components',
    components: {
        PostList,
        CreatePost,
        }
        
    }
</script>

<style scoped>

</style>