<template>
    <div class="hair_price">
        <h2>Прайс лист Hair</h2>
        <div class="price_list">
            <div class="price_list_left">
                <h4>Services:</h4>
            </div>
            <div class="price_list_right">
                <p>Майстер</p>
                <p>Топ Майстер</p>
            </div>
        </div>
        <div class="price_list"
            v-for="service in servises"
            :key="service.id"
        >
            <div class="price_list_left">
                <i class="fa-regular fa-circle-check"></i>
                <p>{{service.title}}</p>
            </div>
            <div class="price_list_right">
                <p><strong>{{service.price}}</strong></p>
                <p><strong>{{service.topPrice}}</strong></p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            servises: [
                {id: 1, title: 'Консультація Hair-стиліста', price: '0 ₴', topPrice: '0 ₴'},
                {id: 2, title: 'Стрижка жіноча', price: '1115 ₴', topPrice: '1315 ₴'},
                {id: 3, title: 'Стрижка чубчика /Корекція форми стрижки (без миття голови)', price: '1115 ₴', topPrice: '1315 ₴'},
                {id: 3, title: 'Стрижка чубчика /Корекція форми стрижки (з миттям голови і укладанням рівного волосся на браш)', price: '1115 ₴', topPrice: '1315 ₴'},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.hair_price{
    max-width: 1230px;
    padding: 40px 20px;
    margin-bottom: 50px;
    h2{
        margin-bottom: 40px;
    }
}
.price_list{
    display: grid;
    grid-template-columns: 2fr 1fr;
    border-bottom: 1px solid rgb(75, 75, 75);
    padding: 15px 0;
}
.price_list_left{
    display: flex;
    align-items: center;
    justify-content: flex-start;
    column-gap: 20px;
    p{
        text-align: left;
    }
    @media (max-width: 450px) {
        column-gap: 5px;
        font-size: 12px;
    }
}
.price_list_right{
    display: flex;
    align-items: center;
    justify-content: space-around;
    column-gap: 5px;
    max-width: 150px;
    p{
        @media (max-width: 450px) {
            font-size: 12px;
        }
    }
}
</style>