<template>
                    <div>
                                        <h3 v-for="name in names" :key="name.firstName">
                                        <!-- <{{ name.firstName }} {{ name.lastName }}> -->
                                        <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
                    </h3>
                    </div>
                    
</template>

<script>
export default {
                    name: 'NameList',
                    data() {
                                        return {
                                                            names: [
                                                                                {
                                                                                firstName: 'Bruce',
                                                                                lastName:'Wayne',
                                                                                },
                                                                                 {
                                                                                firstName: 'Clark',
                                                                                lastName:'Kent',
                                                                                },
                                                                                 {
                                                                                firstName: 'Princess',
                                                                                lastName:'Diana',
                                                                                },
                                        ],
                                     }                       
                                        },
                                        
                    }
</script>

<style scoped>
div{
                    width:200px;
                    border:1px solid black;
                    /* height:500px; */
}

</style>