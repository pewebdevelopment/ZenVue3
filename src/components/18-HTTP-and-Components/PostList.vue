<template>
                    <div>
                                        <button class="btn" @click="getPosts">Load Post</button>
                                        <div v-for="post in posts" :key="post.id">
                                        <h3>{{ post.id }} {{ post.title }}</h3>

                                        <p>{{ post.body }}</p>
                                        <hr/>
                    </div>

                    </div>
</template>

<script>
import axios from 'axios'
export default {
       name: 'PostList',
       created() {
              this.getPosts()
       },
                    data() {
                                        return {
                                                            posts: [],
                                        }
                    },
                    methods: {
                                        getPosts() {
                                                            axios.get('https://jsonplaceholder.typicode.com/posts')
                                                                                .then((response) => {
                                                                                                    console.log(response.data)
                                                                                                    this.posts=response.data
                                                                                })
                                                                                .catch((error) => {
                                                                                                    console.log(error)
                                                                                }
                                                                                )
                                        
                                                            
                                               },     
                                        }
                    }
                                        
                    
</script>

<style scoped>

</style>