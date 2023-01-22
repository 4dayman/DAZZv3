<template>
    <div class="container">
        <div class="footer">
                    <div class="header_logo">
            <router-link to="/">
                <h2 class="header_logo_main">DAZZ</h2>
                <span class="header_logo_desc">beauty space</span>
            </router-link>
        </div>

            <div class="menu_social">
                    <a href="#">
                        <i class="fa-brands fa-facebook"></i>
                        <!-- <img src="@/assets/socialIcons/Instagram.svg" alt=""> -->
                    </a>
                    <a href="#">
                        <i class="fa-brands fa-instagram"></i>
                        <!-- <img src="@/assets/socialIcons/Facebook.svg" alt=""> -->
                    </a>
                    <a href="#">
                        <i class="fa-brands fa-telegram"></i>
                        <!-- <img src="@/assets/socialIcons/YouTube.svg" alt=""> -->
                    </a>
                </div>
                <div class="footer_copy">&#169;Copyright, 2023. Dazz</div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container{
    background: rgba(0, 0, 0, 0.8);
    height: 80px;
    padding-top: 10px;
}
.footer{
    max-width: 1230px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
}
.header_logo_main{
    font-family: 'Kanit', sans-serif;
    font-size: 30px;
    font-weight: 600;
    color: rgba(155, 155, 155, 0.637);
    text-shadow: 1px 1px 30px gray, 0 0 1em rgb(201, 201, 204), 0 0 0.2em rgb(162, 162, 173);
     -webkit-text-stroke: 1px rgba(80, 80, 80, 0.726);
     margin-bottom: -10px;
}
.header_logo_desc{
    font-family: 'Playfair Display', serif;
    font-size: 10px;
    letter-spacing: 1.5px;
    color: #c7bd95;
    text-transform: uppercase;
}
.menu_social {
    i{
        margin-right: 15px;
        opacity: 0.8;
        font-size: 30px;
        color: #868686;
        &:hover {
            opacity: 1;
        }
    }
}
.footer_copy{
    font-family: 'Kanit', sans-serif;
    margin-top: 5px;
    font-size: 10px;
    letter-spacing: 1.5px;
    color: rgba(155, 155, 155, 0.637);
}
</style>