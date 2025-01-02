<script setup>
  import { ref } from 'vue';
  const backgroundInfo = ref('background-info');
</script>

<template>
    <div v-bind:class="backgroundInfo">
        <div class="info">
            <section class="phone-info">
                <span><i class="fa-solid fa-phone"></i></span>
                <span><p class="phone-info-text">(414) 857 - 0107</p></span>
            </section>
            <section class="mail-info">
                <span><i class="fa-solid fa-envelope"></i></span>
                <span><p class="mail-info-text">feastifyfoods@gmail.com</p></span>
            </section>
        </div>
        <div class="socials">
            <span><i class="fa-brands fa-twitter"></i></span>
            <span><i class="fa-brands fa-facebook"></i></span>
            <span><i class="fa-brands fa-instagram"></i></span>
            <span><i class="fa-brands fa-github"></i></span>
        </div>
    </div>
    
  </template>

  
  <style scoped>
  .background-info
  {
    background-color:#474747;
    display: flex;
    justify-content: space-around;
    align-items: center;
    width:100%;
    padding:6px;
    color:#fff;
    font-size: 12px;
  }

  .info
    {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 20px;

        section
        {
            display: flex;
            flex-direction: row;
            align-items: center;
            gap: 5px;
        }
        
    }
    section span i
    {
        color: white;
    }
    .socials
    {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 5px;

        span
        {
            background-color: #8a8888;
            border-radius: 100%;
            display: flex;
            justify-content: center;
            width: 20px;
            padding: 4px 0;
        }
    }
  </style>