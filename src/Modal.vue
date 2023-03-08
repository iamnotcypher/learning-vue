<template>
  <div class="backdrop">
    <div class="modal">
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Optio, in.</p>
    </div>
  </div>
</template>

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
    background: rgba(0,0,0,0.5);
    width: 100%;
    height: 100%;
  }
</style>