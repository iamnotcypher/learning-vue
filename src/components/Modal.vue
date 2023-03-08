<template>
  <div class="backdrop">
    <div class="modal" :class="{ sales: theme === 'sales' }">
      <h1>{{ header }}</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus recusandae totam facere officia eum! Inventore possimus assumenda eligendi ipsa magni.</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['header', 'theme']
}
</script>

<style scoped>
  .modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: #fff;
    border-radius: 5px;
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