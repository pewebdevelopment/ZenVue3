<template>
                    <div>
<button  @mouseover="incrementCount">Hoverd {{ count }} times</button>
                    </div>
</template>

<script>
                    export default {
                    name: 'hoverCounter',
                    data() {
                                        return {
                                        count:0                    
                                        }
                    },
                    methods: {
                                        incrementCount() {
                                                            this.count +=1
                                        }
                    }
                    }
</script>

<style scoped>

</style>