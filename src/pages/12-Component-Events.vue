<template>
  <div>
    <button @click="showPopup=true">Show Popup</button>
    <Popup v-show="showPopup" @close="closePopup"/>
  </div>
</template>

<script>
import Popup from "../components/12-Component-Events/Popup.vue";
export default {
  name: '12-Component-Events',
  components: {
    Popup,
  },
  data() {
    return {
    showPopup:false,  
    }
  },
  methods: {
    closePopup(name) {
      this.showPopup = false
      console.log('name' , name)
    }
  }
};
</script>

<style scoped></style>
