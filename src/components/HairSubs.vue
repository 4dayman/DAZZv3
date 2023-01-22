<template>
    <div class="services_wrapper">
        <div class="services">
            <h2>З цією послугою можна зробити паралельно</h2>
            <div class="services_cards">
                <router-link to="/about" class="services_card">
                    <img src="@/assets/nails_1.jpg" alt="">
                    <div class="card_text">
                        <h2>Nails</h2>
                        <h4>To service <i class="fa-solid fa-arrow-right"></i></h4>
                    </div>
                </router-link>
                <router-link to="/about" class="services_card">
                    <img src="@/assets/lush_brow.png" alt="">
                    <div class="card_text">
                        <h2>Lush & Brow</h2>
                        <h4>To service <i class="fa-solid fa-arrow-right"></i></h4>
                    </div>
                </router-link>
                <router-link to="/about" class="services_card">
                    <img src="@/assets/mack_up_1.jpg" alt="">
                    <div class="card_text">
                        <h2>Make Up</h2>
                        <h4>To service <i class="fa-solid fa-arrow-right"></i></h4>
                    </div>
                </router-link>
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.services_wrapper{
    max-width: 1230px;
    padding: 0 20px;
    margin: 0 auto;
}
.services {
    margin-bottom: 50px;
    h2{
        margin-bottom: 20px;
    }
}
.services_cards {
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: 20px;
    row-gap: 20px;
    @media (max-width: 768px) {
        grid-template-columns: 1fr 1fr;
        
    }
    @media (max-width: 425px) {
        grid-template-columns: 1fr;
        
    }
}
.services_card{
    position: relative;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
.card_text{
    position: absolute;
    bottom: 20px;
    left: 20px;
    text-shadow: 1px 1px 15px rgb(0, 0, 0);
    h2, h4{
        color: rgb(238, 238, 238);
    }
}
</style>