<template>
                    <div>
                                        <h2>{{ name }}</h2>
                                        <button class="btn" @click="setName">Change Name</button>

                                        <h2>{{ count }}</h2>
                                        <button class="btn" @click="incrementCount">Increment Count</button>

                                        <h2>{{ first }} {{ last }}</h2>
                                         <button class="btn" @click="changeHero">Change Hero</button>

                    </div>
</template>

<script>
import {ref , reactive , toRefs} from 'vue'
                    export default {
                    name: 'Methods',
                    setup() {
                                        const count = ref(0)
                                        function incrementCount() {
                                                            count.value++;
                                        }

                                        const state = reactive({
                                                            first: 'Bruce',
                                                            last:'Wayne',
                                        })

                                       
                                        function changeHero() {
                                                            state.first = 'Clark'
                                                            state.last = 'Kent'
                                        }
                                        return{
                                                            count,
                                                            incrementCount,
                                                            ...toRefs(state),
                                                            changeHero,
                                        }
                    },
                    data(){
                                              return {
                                                             name:'Vishwas', 
                                        }
                    },
                    methods: {
                                        setName() {
                                                            this.name = 'Codevolution'
                                        }
                    },           
                    }
</script>

<style scoped>

</style>