<template>
    <div class="parent">
      <h2>Parent Component</h2>
      <p>Data from Child: {{ childData }}</p>
      <ChildOne @data-from-child="handleDataFromChild" />
      <ChildTwo @data-from-child="handleDataFromChild" />
    </div>
  </template>
  
  <script>
  import ChildOne from './childone.vue';
  import ChildTwo from './childtwo.vue';
  
  export default {
    name: 'Parent',
    components: {
      ChildOne,
      ChildTwo
    },
    data() {
      return {
        childData: ''
      };
    },
    methods: {
      handleDataFromChild(data) {
        this.childData = data;
      }
    }
  }
  </script>
  
  <style scoped>
  .parent {
    background-color: #8d9bcb;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .parent h2 {
    color: #333;
  }
  
  .parent p {
    color: #666666;
  }
  
  /* You can add more styles as needed */
  </style>
  