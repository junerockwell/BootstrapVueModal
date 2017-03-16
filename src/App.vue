<template>
<div id="wrapper" class="container"> 
 <modal v-if="showModal"> 
  <h3 slot="header" class="modal-title">
    Modal title
  </h3>
  
  <div slot="body">
    <img src="./assets/logo.png" />
  </div>

  <div slot="footer">
   <button type="button" class="btn btn-outline-info" @click="closeModal()"> Close </button>
   <button type="button" class="btn btn-primary" data-dismiss="modal" @click="submitAndClose()">
     Submit
   </button>
  </div>
</modal>
  <button type="button" class="btn btn-primary" @click="openModal()">Open Modal</button>
 </div>
</template>

<script>
// import it
import Modal from './components/Modal';

export default {
  // register it as a component
  components: {
    Modal
  }, 
  data() { 
    return { 
      showModal: false 
    } 
  }, 
 methods: { 
   openModal() { 
     this.showModal = true; 
   } ,
  closeModal() {
     this.showModal = false;
  },
  submitAndClose() {
  
  }
 }  
}
</script>

<style>
#wrapper {
  margin-top: 60px;
}
</style>
