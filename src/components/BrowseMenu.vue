<script setup>
import { ref } from 'vue';

const menuOptions = ref([
    {name:'Breakfast', url:'/tea 1.png', description:'In the new era of technology we look in the future with certainty and pride for our life.', altText:'breakfast'},
    {name:'Main Dishes', url:'/Vector (9).png', description:'In the new era of technology we look in the future with certainty and pride for our life.', altText:'maindishes'},
    {name:'Drinks', url:'/Vector (8).png', description:'In the new era of technology we look in the future with certainty and pride for our life.',altText:'drink'},
    {name:'Desert', url:'/Group (2).png', description:'In the new era of technology we look in the future with certainty and pride for our life.', altText:'desert'},
])
</script>

<template>
    <div>
        <h2>Browse our Menu</h2>
        <section>
            <figure v-for="menu in menuOptions"> 
                <img :src="menu.url" :alt="menu.altText">
                <figcaption> {{ menu.name }}</figcaption>
                <figcaption>{{ menu.description }}</figcaption>
                <p><a href="">Explore Menu</a></p>
            </figure>
        </section>
    </div>
</template>

<style scoped>
div 
{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 40px 0;
}
section
{
    display: flex;
    width: 80%;
    margin: auto;
    gap: 30px;
    margin-top: 20px;
}
figure
{
    border: 2px solid #DBDFD0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    column-gap: 30px;
    padding: 20px 10px;
}
img 
{
    width: 50px;
    margin: 20px 0;
}
</style>