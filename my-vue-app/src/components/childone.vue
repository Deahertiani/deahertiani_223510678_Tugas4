<template>
    <div class="child-one">
      <h3>Child One</h3>
      <button @click="sendData">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'childone',
    methods: {
      sendData() {
        this.$emit('data-from-child', 'Data from child one');
      }
    }
  }
  </script>
  
  <style scoped>
  .child-one {
    background-color: #08024b;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .child-one h3 {
    color: #333;
  }
  
  .child-one button {
    background-color: #007bff;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 10px;
  }
  
  .child-one button:hover {
    background-color: #0056b3;
}
</style>