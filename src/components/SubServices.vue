<template>
    <div class="main_desc_wrapper">
        <div class="main_desc">
            <div class="desc_left">
                <h2>Паралельні послуги</h2>
                <p>Зона паралельних послуг в Dazz — це місце нашої з вами максимальної продуктивності або тотального релаксу. Поки ви налаштовуєтесь на важливу подію, фотозйомку, ділову зустріч або вечірку, майстри Dazz виконають до 3 послуг одночасно. Скомбінувати кількість і види паралельних послуг ми можемо на ваш смак</p>
            </div>
            <div class="desc_right">
                <img src="@/assets/bg_subs.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.main_desc_wrapper{
margin-top: 50px;
}
.main_desc {
    position: relative;
    max-width: 1230px;
    padding: 0 20px;
    display: grid;
    margin: 0 auto;
    grid-template-columns: 1fr 1fr;
    margin-bottom: 50px;
    column-gap: 20px;
    @media (max-width: 475px) {
        grid-template-columns: 1fr;
        row-gap: 20px;
    }
}
.desc_left,
.desc_right {
    max-width: 100%;
}
.desc_left{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    text-align: left;
    color: #41456B;
    @media (max-width: 475px) {
        align-items: center;
        text-align: center;
    }
    p{
        font-weight: 400;
        font-size: 16px;
        line-height: 180%;
        letter-spacing: 0.02em;
        text-align: justify;
    }
}
.desc_right{
    height: 100%;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        opacity: 0.8;
    }
}
</style>




<script>
export default {
    
}
</script>

<style lang="scss" scoped>
.sub_services {
    max-width: 1230px;
    margin: 0 auto;
    padding: 40px 20px;
    h4{
        text-align: justify;
    }
}
</style>