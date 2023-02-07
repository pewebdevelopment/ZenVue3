<template>
            <div class="card">
                    <!-- <slot></slot> -->
                    <div id="card-header">
                                        <slot name="header"></slot>
                    </div>
                     <div id="card-content">
                                        <slot></slot>
                    </div>
                     <div id="card-footer">
                                        <slot name="footer"></slot>
                    </div>

            </div>       
</template>

<script>
export default {
                                        name:'card'
                                        
                    }
</script>

<style scoped>
.card{
                    width:200px;
                    margin-bottom:20px;
                    padding:16px;
                    border:1px solid black;
}

</style>