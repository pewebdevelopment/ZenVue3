<template>
                    <h2>{{ name }}</h2>
                    <div>
                                        <button class="btn" v-on:mouseover="name= 'Batman'">Change name</button>
                                        <button class="btn" v-on:click="changeName, increment(1,$event)">Change Name</button>
                    </div>
                    <h2>{{ count }}</h2>
                    <div>
                                        <button class="btn" v-on:click="increment(1 , $event)">Increment 1</button>
                                        <button class="btn" v-on:click="increment(5)">Increment 5</button>
                                        <button class="btn" v-on:click="decrement(1)">Decrement 1</button>
                                        <button class="btn" v-on:click="decrement(5)">Decrement 5</button>
                    </div>
                    
</template>

<script>
export default {
                    name: 'Event-Handling-v-on',
                    data() {
                                        return {
                                                            name: 'Vishwas',
                                                            count:0
                                                            }
                    },
                    methods: {
                                        changeName(event) {
                                                            this.name = 'Batman'
                                                            console.log('Event', event)
                                        },
                                        increment(num) {
                                                            this.count+=num
                                        },
                                        decrement(num) {
                                                            this.count-=num
                                        }
                                                            
                    },
                                        
                    }
</script>

<style scoped>


</style>