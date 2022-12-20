

<template>
  <h1 class="font-mono text-center text-3xl ">{{title}}</h1>
  <div v-if="showModel">
    <Modal :text="text" :header="header" theme="sale" @close="toggleModel"/>

  </div>
  <div class="flex justify-center items-center">
    <button class="py-2 px-5 bg-slate-900 text-white font-bold font-mono "
            @click="toggleModel">Show Modal
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
      showModel: false,
    };
  },
  methods: {
    toggleModel() {
      this.showModel = !this.showModel;
    },

  }

}

</script>



<style>

</style>
