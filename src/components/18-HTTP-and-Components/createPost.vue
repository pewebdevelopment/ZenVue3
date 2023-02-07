<template>
                    <div>
                                        <form @submit.prevent="createPost">
                                                            <div>
                                                                                <label for="userId">Post User</label>
                                                                                <input type="text" id="userId" v-model="formData.userId">
                                                            </div>

                                                             <div>
                                                                                <label for="title">Post title</label>
                                                                                <input type="text" id="title" v-model="formData.title">
                                                            </div>

                                                            <div>
                                                                                <label for="body">Post Body</label>
                                                                                <input type="text" id="body" v-model="formData.body">
                                                            </div>
                                                            <button class="btn">Create Post</button>
                                        </form>

                    </div>
</template>

<script>
import axios from 'axios'
                    export default {
                                        name:'createPost',
                    data() {
                                        return {
                                                            formData: {
                                                                                                    userId: '',
                                                                                                    title: '',
                                                                                                    body:''
                                                            }
                                        }
                    },
                    methods: {
                                        createPost(){
                                                            axios.post('https://jsonplaceholder.typicode.com/posts', this.formData)
                                        .then((response) => {
                                                            console.log(response.data)
                                                            this.posts=response.data
                                                                                })
                                        .catch((error) => {
                                                            console.log(error)
                                                                                })
                             }           
                    }
                    }
</script>

<style scoped>

</style>