<template>
  <div @click.self="closeModal" class="backdrop">
    <div class="modal" :class="{ sales: theme === 'sales' }">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ['theme'],
  methods: {
    closeModal() {
      this.$emit('close')
    }
  }
}
</script>

<style scoped>
  .modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: #fff;
    border-radius: 8px;
    border: 1px solid #fff
  }
  .backdrop {
    position: fixed;
    top: 0;
    left: 0;
    background: rgba(0,0,0,0.5);
    width: 100%;
    height: 100%;
  }
  h1 {
    color: #03cfb4;
    border: none;
    padding: 0;
  }
  .modal.sales {
    background: crimson;
    color: white;
  }
  .modal.sales h1 {
    color: white;
  }
</style>