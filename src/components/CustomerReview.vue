<script setup>
import { ref } from 'vue';

const customerReviews = ref([
  {
    id: 1,
    topic: 'The best restaurant',
    text: 'Last night, we dined at place and were simply blown away. From the moment we stepped in, we were enveloped in an inviting atmosphere and greeted with warm smiles.',
    authorId: 1
  },
  {
    id: 2,
    topic: 'Simply Delicious',
    text: 'Place exceeded my expectations on all fronts. The ambiance was cozy and relaxed, making it a perfect venue for our anniversary dinner. Each dish was prepared and beautifully presented.',
    authorId: 2
  },
  {
    id: 3,
    topic: 'One of a Kind',
    text: 'The culinary experience at place is first to none. The atmosphere is vibrant, the food - nothing short of extraordinary. The food was the highlight of our evening. Highly recommended.',
    authorId: 3
  }
]);

const customerProfiles = ref([
  {
    id: 1,
    url: '/Ellipse 19.png',
    firstName: 'Sophie',
    lastName: 'Robson',
    location: 'Los Angeles, CA'
  },
  {
    id: 2,
    url: '/Image (1).png',
    firstName: 'Matt',
    lastName: 'Canon',
    location: 'San Diego, CA'
  },
  {
    id: 3,
    url: '/profile pic.png',
    firstName: 'Andy',
    lastName: 'Smith',
    location: 'San Francisco, CA'
  }
]);
</script>

<template>
  <div class="customerReview-container">
    <h2>What Our Customers Say</h2>
    
    <div class="customer-review">
      <section class="review">
        <figure v-for="review in customerReviews" :key="review.id">
          <figcaption>
            <p class="review-topic">"{{ review.topic }}"</p>
          </figcaption>
          <figcaption>
            <p class="review-text">{{ review.text }}</p>
          </figcaption>
          <hr>
          
          
          <div class="profile-info" v-if="customerProfiles.find(profile => profile.id === review.authorId)">
            <img 
              :src="customerProfiles.find(profile => profile.id === review.authorId).url" 
              :alt="customerProfiles.find(profile => profile.id === review.authorId).firstName"
            >
            <section>
              <p class="name">
                {{ customerProfiles.find(profile => profile.id === review.authorId).firstName }}
                {{ customerProfiles.find(profile => profile.id === review.authorId).lastName }}
              </p>
              <p>
                {{ customerProfiles.find(profile => profile.id === review.authorId).location }}
              </p>
            </section>
          </div>
        </figure>
      </section>
    </div>
  </div>
</template>

<style scoped> 
.customerReview-container
{
    width:80%;
    margin: 60px  auto;
    padding: 30px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    
}
h2{
    font-size: 35px;
    margin: 30px 0;
    color: #2C2F24;
}
.customer-review .review
{
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 30px;
}
figure
{
    background-color: #F9F9F7;
    padding: 20px;
    border-radius: 20px;
}
figcaption .review-topic
{
    color:#AD343E;
    font-weight: bold;
    margin: 8px 0;
}
figcaption .review-text
{
    font-size: 12px;
    color: #2C2F24;
    padding: 10px 0;
    line-height: 20px;
   
}
.profile-info
{
    display: flex;
    flex-direction: row;
    margin: 20px 0;
    gap: 10px;
    img 
    {
        width: 40px;
        height: 40px;
    }

    section 
    {
        display: flex;
        flex-direction: column;
        p 
        {
            font-size: 12px;
            padding: 2px 0;
        }
        .name
        {
            font-weight: bold;
        }
        
    }
}
</style>