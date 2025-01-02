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
        <h1>Browse our Menu</h1>
        <section>
            <figure v-for="menu in menuOptions"> 
                <img :src="menu.url" :alt="menu.altText">
                <figcaption><span class="name"> {{ menu.name }}</span></figcaption>
                <figcaption><span class="description">{{ menu.description }}</span></figcaption>
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
h2
{
    margin: 20px;
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
    text-align: center;
    border-radius: 20px;

    p
    {
        margin: 20px  0;

        a
        {
            color:#AD343E;
            text-decoration: none;
            font-size: 15px;
            font-weight: bold;
        }
    }
}
img 
{
    width: 50px;
    height: 50px;
    margin: 40px 0;
}

</style>
<style>
figcaption
{
    margin: 10px 0;
}
figcaption .name
{
    color: #2C2F24;
    font-weight: bold;
    font-size: 18px;

}
figcaption .description
{
    color: #2C2F24;
    font-size: 14px;
    
}
</style>