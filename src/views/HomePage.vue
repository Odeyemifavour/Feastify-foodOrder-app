<script setup>
  import TopBar from '@/components/TopBar.vue';
  import HeaderBar from '@/components/HeaderBar.vue';
  import { ref } from 'vue';
  const heroBackground = ref('background');

</script>
<template>
  <div class="homepage-container">
    <TopBar/>
    <HeaderBar/>
    <div v-bind:class="heroBackground" >
      <div class="hero-content">
        <h1>Best food for your taste</h1>
        <p>Discover delectable cuisine and unforgettable moments in our welcoming, culinary haven.</p>
        <section class="hero-btn">
          <button class="book-a-table">book a table</button>
          <button class="explore-menu">explore menu</button>
        </section>
      </div>
    </div>
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
    .background
    {
      background: url('/bg.png');
      background-position: center;
      background-size: cover;
      height:600px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .hero-content
    {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center; 
      position: absolute; 
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;

        h1 
        {
          font-size: 50px;
          color:#2C2F24;
          margin-top: 60px;
          margin-bottom: 10px;
          padding-top: 30px;
        }
         p 
         {
          font-size: 15px;
          color:#2C2F24;
          margin-bottom: 40px;
          width: 70%;
         }
    }
    .hero-btn
    {
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 20px;

      button 
      {
        width: 130px;
        height:50px;
        text-transform: capitalize;
        border-radius: 30px;
        cursor: pointer;
      } 
    }
    .book-a-table
        {
          background-color: #AD343E;
          color: white;
          border: none;
        }
    .explore-menu
      {
        color:#2C2F24;
        background: transparent;
        border: 2px solid #2C2F24;
      } 
  </style>