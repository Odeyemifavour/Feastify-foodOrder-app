<script setup>
import { ref } from 'vue';
const headerLogoText = ref('bold');
const activeMenu = ref('active');
</script>
<template>
    <div class="headerBar-container">
        <section class="header-logo">
            <span><img src="/Vector (7).png" alt=""></span>
            <span :class="headerLogoText" style="font-size: 30px;" >Feastify</span>
        </section>
        <section class="header-menu">
            <ul>
                <li :class="activeMenu">home</li>
                <li>about</li>
                <li>menu</li>
                <li>pages</li>
                <li>contact</li>
            </ul>
        </section>
        <section class="header-btn">
            <button>book a table</button>
        </section>
    </div>
</template>
<style scoped>
    .headerBar-container
    {
        display: flex;
        justify-content: space-around;
        align-items: center;
        width:100%;
        color:#2C2F24;
        margin: 5px 0;
    }
    .bold
    {
        font-weight: bold;
    }
    .header-logo
    {
        display: flex;
        flex-direction: row;
        align-items: center;

        
    }
    .header-menu 
    {
        ul 
        {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: center;
            gap: 10px;

            li
            {
                list-style-type: none;
                font-size: 13px;
                padding: 8px 15px;
                border-radius: 25px;
                text-transform:capitalize;
                cursor: pointer;
                font-weight: 500;
            }
        }
    }
    .active 
    {
        background-color:#DBDFD0;
    }
    .header-btn
    {
        button
        {
            background: transparent;
            border: 2px solid #2C2F24;;
            width: 100px;
            border-radius: 30px;
            padding: 10px 0;
            cursor: pointer;
            text-transform: capitalize;
            font-size: 13px;
        }
    }
</style>