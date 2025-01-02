<script setup>
   
import { ref } from 'vue';

    const uniqueServices = ref([
        {name:'Catering', url:'/kebab-set-table 1.png', description:'In the new era of technology we look in the future with certainty for life.', altText:'Catering'},
        {name:'Birthdays', url:'/Mask group (1).png', description:'In the new era of technology we look in the future with certainty for life.', altText:'Birthdays'},
        {name:'Weddings', url:'/happy-man-wife-sunny-day 1.png', description:'In the new era of technology we look in the future with certainty for life.', altText:'Weddings'},
        {name:'Events', url:'/group-friends-eating-restaurant 1.png', description:'In the new era of technology we look in the future with certainty for life.', altText:'Events'},
    ])
</script>

<template>
    <div  class="uniqueServices-container">
        <h1>We also offer unique services for your events</h1>
        <div class="services">
            <section>
                <figure v-for="uniqueService in uniqueServices ">
                    <img :src="uniqueService.url" :alt="uniqueService.altText">
                    <figcaption> <span class="name">{{ uniqueService.name }}</span></figcaption>
                    <figcaption> <span class="description">{{ uniqueService.description }}</span></figcaption>
                </figure>
            </section>
        </div>
    </div>
</template>

<style scoped>
.uniqueServices-container
{
    margin: 40px;
    color:#2C2F24;
}
h1
{
    margin: 20px 0;
    padding: 10px 0;
    font-size: 30px;
}
section
{
    display: flex;
    flex-direction: row;
    align-items: center;
}
img
{
    border-radius: 20px;
}
</style>