<template>
                    <div>
                    <!-- <h2>{{ state.firstName }} {{state.lastName}}</h2> -->
                    <h2>{{ fname }} {{ lname }}</h2>
                    <h2>{{firstName}} {{ lastName }}</h2>
                    </div>
</template>

<script>
import {reactive , toRefs} from 'vue'
                    export default {
                    name: 'DemoTwo',
                    data() {
                                        return {
                                        fname: 'Bruce',
                                        lname: 'Wayne',
                                                            
                                        }
                    },
                    setup() {
                                       const state =  reactive({
                                                            firstName : 'Bruce',
                                                            lastName :"Wayne"
                                       })
                                        setTimeout(() => {
                                                  state.firstName='Clark'
                                                  state.lastName='Kent'          
                                        } , 2000 )

return toRefs(state)
                                        // return {
                                        //                     firstName: state.firstName,
                                        //                     lastName:state.lastName
                                        // }
                                                            
                                        },
                    }
</script>

<style scoped>

</style>