

<template>
  <h1 class="font-mono text-center text-3xl ">{{title}}</h1>
  <div v-if="showModel">
    <Modal theme="sale" @close="toggleModel">
      
      <template v-slot:links>
        <a href="#">Sign Up For Now</a>
        <a href="#">More info</a>
      </template>
      
      <h1 class="font-mono text-center text-3xl ">hey this is Tamzids Dick</h1>
      <p>Grab his dick for 5 minutes</p>



    </Modal>

  </div>





  <div v-if="ShowModelTwo">
    <Modal  @close="toggleModelTwo">

      <h1 class="font-mono text-center text-3xl ">Sign Up For NewsLatter</h1>
      <p>For updates and Promo Codes</p>
    </Modal>

  </div>
  <div class="flex justify-center items-center">
    <button class="py-2 px-5 bg-slate-900 text-white font-bold font-mono "
            @click="toggleModel">Show Modal
    </button>

  </div>
  <div class="flex justify-center items-center mt-10">
    <button class="py-2 px-5 bg-slate-900 text-white font-bold font-mono "
            @click="toggleModelTwo">Show Modal
    </button>

  </div>

</template>

<script>

import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {Modal},
  data() {
    return {
      title: "Hello World",
      header: "Sign Up For the giveway",
      text: "Grab your Ninja swag for half price",
      showModel: false,
      ShowModelTwo: false,

    };
  },

  methods: {
    toggleModel() {
      this.showModel = !this.showModel;
    },
    toggleModelTwo() {
      this.ShowModelTwo= !this.ShowModelTwo;
    },

  }

}

</script>



<style>

</style>
