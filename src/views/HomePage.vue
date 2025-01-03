<script setup>
  import { ref } from 'vue';
  import TopBar from '@/components/TopBar.vue';
  import HeaderBar from '@/components/HeaderBar.vue';
  import BrowseMenu from '@/components/BrowseMenu.vue';
  import AboutCard from '@/components/AboutCard.vue';
  import UniqueServices from '@/components/UniqueServices.vue';
  import CustomerReview from '@/components/CustomerReview.vue';

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

    <BrowseMenu/>

    <div class="about-container">
      <AboutCard/>
    </div>

    <div class="unique-services">
      <UniqueServices/>
    </div>

    <div class="food-delivery-info">
      <div class="images">
        <img src="/mid-shot-chef-holding-plate-with-pasta-making-ok-sign 1.png" alt="">
        <section>
          <img src="/sour-curry-with-snakehead-fish-spicy-garden-hot-pot-thai-food 1.png" alt="">
          <img src="/sadj-iron-pot-with-various-salads 1.png" alt="">
        </section>
      </div>
      <div class="text">
        <h2>Fastest Food Delivery in City</h2>
        <p>Our visual designer lets you quickly and of drag a down your way to customapps for both keep desktop. </p>
        <section class="delivery-desc">
          <p>
            <span><img src="/Icon.png" alt=""></span>
            <span>Delivery within 30 minutes</span>
          </p>
          <p>
            <span><img src="/Icon (1).png" alt=""></span>
            <span>Best Offer & Prices</span>
          </p>
          <p>
            <span><img src="/Icon (2).png" alt=""></span>
            <span>Online Services Available</span>
          </p>
        </section>
      </div>
    </div>

    <div class="customer-review">
      <CustomerReview/>
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
      .about-container
      {
        background-color: #F9F9F7;
        padding: 30px 0;
      }
      .unique-services
      {
        background-color: #ffffff;
        padding: 30px 0;
      }
      .food-delivery-info
      {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 80%;
        margin:  80px auto;
        gap: 30px;
        color:#2C2F24;

          .images
          {
            display: flex;
            flex-direction: row;
            gap: 20px;

            section 
            {
              display: flex;
              flex-direction: column;
              gap: 20px;
              margin-top: 50px;
              
            }
          }
          .text 
          {
            display: flex;
            flex-direction: column;

            h2
            {
              
              font-size: 35px;
              width: 90%;
            }
            p 
            {
              font-size: 11px;
              margin: 10px 0;
            }

            section p 
            {
              display: flex;
              flex-direction: row;
              align-items: center;
              gap: 10px;

              span 
              {
                font-size: 13px;
                font-weight: bold;
              }
            }
          }

      }
.customer-review
{
  background-color: white;
}      
  </style>