<template>
  <div class="top-0 fixed bg-[rgba(0,0,0,0.5)]  w-full h-full" @click.self="closeModal">
    <div class="modal w-[400px] p-5 mx-auto my-20 bg-white rounded-2xl" :class="{ sale: theme === 'sale' }">

      <slot></slot>
      <div class="actions">

        <slot name="links"></slot>

      </div>

    </div>

  </div>




</template>

<script>

export default {
  name: "Modal",
  props: ["header", "text", "theme"],
  methods: {
    closeModal() {
      this.$emit('close');
    },
  },
}
</script>

<style >
.sale{
  background-color: rgba(255, 213, 1, 0.65);
}
</style>