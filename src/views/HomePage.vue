<script setup>
  import TopBar from '@/components/TopBar.vue';
  import HeaderBar from '@/components/HeaderBar.vue';
</script>
<template>
  <div class="homepage-container">
    <TopBar/>
    <HeaderBar/>
  </div>
</template>
  
  <style >
  *{
    margin:0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Montserrat", serif;
  }

  </style>
  <style scoped>
    .homepage-container
    {
      width: 100%;
      height: 100vh;
    }
  </style>