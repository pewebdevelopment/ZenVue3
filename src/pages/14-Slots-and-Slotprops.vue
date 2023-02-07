<template>
    <div >
        <div class="container">
             <Card> Card content </Card>
             <Card>
                    <h2>Card content</h2>
             </Card>

             <Card>
                <template v-slot:header>
                    <h3>Header</h3>
                </template>
                <template v-slot:default>
                    <h3>Default </h3>
                </template>
                <template v-slot:footer>
                    <h3>footer</h3>
                </template>
             </Card>

              <NameList>
                <template v-slot:default="slotProps">
                    {{ slotProps.firstName }} {{ slotProps.lastName }}
                    {{ slotProps.lastName }} {{ slotProps.firstName }}
                    {{ slotProps.firstName }}

                </template>
              </NameList>
            </div>
    </div>

   
</template>

<script>
import Card from '../components/14-Slots-and-Slotprops/card.vue'
import NameList from '../components/14-Slots-and-Slotprops/NameList.vue'
export default {
    name: '14-Slots-and-Slotprops',
      components: {
          Card, 
                                          NameList,                 
                                        }
        
    }
</script>

<style scoped>
.container{
    width:70%;
    margin:auto;
    
}


</style>