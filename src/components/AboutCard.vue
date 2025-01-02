<script setup></script>

<template>
    <div class="about-container">
        <div class="about-card">
            <div class="about-img">
                <img src="/Image.png" alt="image">
            </div>
            <div class="overlap" >
                <h3>Come and visit us</h3>
                <p>
                    <span><i class="fa-solid fa-phone"></i></span>
                    <span>(414) 857 - 0107</span>
                </p>
                <p>
                    <span><i class="fa-solid fa-envelope"></i></span>
                    <span>feastifyfoods@gmail.com</span>
                </p>
                <p>
                    <span><i class="fa-solid fa-map"></i></span>
                    <span>837 W. Marshall Lane Marshalltown, IA 50158, Los Angeles</span>
                </p>
            </div>
        </div>
       
        <div class="about-text">
            <h2>We provide healthy food for your family.</h2>
            <p>Our story began with a vision to create a unique dining experience that merges fine dining, exceptional service, and a vibrant ambiance. Rooted in city's rich culinary culture, we aim to honor our local roots while infusing a global palate.</p>
            <p>At place, we believe that dining is not just about food, but also about the overall experience. Our staff, renowned for their warmth and dedication, strives to make every visit an unforgettable event.</p>
            <button>more about us</button>
        </div>
    </div>
</template>

<style scoped>
.about-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 80%;
    margin: auto;
    gap: 100px;
}

.about-card {
    position: relative; 
    width: 40%;
}

.overlap {
    background-color: #474747;
    height: 200px;
    width: 250px;
    border-radius: 5px;
    position: absolute;
    bottom: -20px;
    right: -20px; 
    z-index: 1; 
    color: white;
    font-size: 12px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 20px;

    h3
    {
        margin:8px 0;
    }
   
}
 .overlap p
    {
        margin: 8px 0;
        display: flex;
        flex-direction: row;
        gap: 8px;
    }

.about-img {
    position: relative;
}

.about-img img {
    width: 400px;
    height: 400px;
    object-fit: cover; 
    border-radius: 5px;
}

.about-text {
    flex: 1;  
    font-size: 12px;
    
    h2
    {
        font-size: 35px;
        width:70%;
        color:#2C2F24;
    }
    p 
    {
        margin: 10px 0;
        font-size: 12px;
        width: 60%;
        color:#2C2F24;
        
    }
    button 
    {
       margin: 20px 0;
       height:50px;
       width: 150px;
       color:#2C2F24;
       border: 2px solid #2C2F24;
       background: transparent;
       border-radius: 30px;
       text-transform: capitalize;
       font-weight: bold;
       cursor: pointer;
    }
}

</style>