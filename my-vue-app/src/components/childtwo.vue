<template>
    <div class="child-two">
      <h3>Child Two</h3>
      <button @click="sendData">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'childtwo',
    methods: {
      sendData() {
        this.$emit('data-from-child', 'Data from child two');
      }
    }
  }
  </script>
  
  <style scoped>
  .child-two {
    background-color: #08024b;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .child-two h3 {
    color: #333;
  }
  
  .child-two button {
    background-color: #007bff;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 10px;
  }
  
  .child-two button:hover {
    background-color: #1f82ec;
  }
  </style>
  