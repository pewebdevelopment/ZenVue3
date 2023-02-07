<template>
                    <div>
<input type="text" placeholder="First Name" v-model="fName"/>
<input type="text" placeholder="Last Name" v-model="lName"/>
<h2>Option Fullname is {{ fullName }}</h2>

<input type="text" placeholder="First Name" v-model="refFirstName"/>
<input type="text" placeholder="Last Name" v-model="refLastName"/>
<h2>Composition Fullname is {{ refFullName }}</h2>

<input type="text" placeholder="First Name" v-model="reactiveFirstName"/>
<input type="text" placeholder="Last Name" v-model="reactiveLastname"/>
<h2>Reactive Fullname is {{ reactiveFullName }}</h2>

</div>

</template>

<script>
import {ref, reactive, toRefs , computed} from 'vue'
                    export default {
                    name: 'Computed',
                    setup() {
                                        const refFirstName = ref('')
                                        const refLastName = ref('')

                                        const refFullName = computed(function () {
                                              return `${refFirstName.value} ${refLastName.value}`           
                                        })

                                        const state = reactive({
                                                            reactiveFirstName: '',
                                                            reactiveLastname: '',
                                        })

                                        const reactiveFullName = computed(function () {
                                                            return `${state.reactiveFirstName} ${state.reactiveLastname}`
                                        })

                                        return {
                                                            refFirstName,
                                                            refLastName,
                                                            refFullName,
                                                            ...toRefs(state),
                                                            reactiveFullName,
                                        }
                    },
                    data() {
                                        return {
                                        fName: '',
                                        lName: '',
 
                                        }
                                        
                    },
                    computed: {
                                        fullName(){
                                        return `${this.fName} ${this.lName}`
                                        }                
                                        },
                    }
</script>

<style scoped>

</style>