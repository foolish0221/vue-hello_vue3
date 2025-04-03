<template>
    <div class="person">
        <h2>一辆{{ car.brand }}车，价值{{car.price}}万元</h2>
        <button @click="changeBrand">修改汽车的品牌</button>
        <button @click="changePrice">修改汽车的价格</button>
        <button @click="changeCar">修改汽车</button>
        <br>
        <h2>游戏列表：</h2>
        <ul>
            <li v-for="item in games":key ="item.id">{{ item.name }}
               
            </li>
            <button @click="changeGameName">修改第一个游戏名字</button>
        </ul>
    </div>
</template>

<script lang="ts" setup>
import { ref,reactive} from 'vue';
    let car = ref({
        brand:'奔驰',
        price:100
    })
    let games = ref([
        {id:'game01' ,name:'王者荣耀'},
        {id:'game02' ,name:'星露谷物语'},
        {id:'game03' ,name:'文明6'},
        {id:'game04' ,name:'黑神话悟空'},
    ])

    function changePrice(){
        car.value.price += 10

    }
    function changeBrand(){
        car.value.brand = '宝马'

    }
    function changeCar(){
        //car = {brand:'奥迪',price:50}
        //Object.assign(car,{brand:'奥迪',price:50})
        car.value = {brand:'奥迪',price:50}
    }
    function changeGameName(){
        games.value[0].name = "饥荒"
    }

</script>

<style scoped>
.person {
    background-color: skyblue;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
}

button {
    margin: 0 5px;
}
li{
    font-size: 20px;
}
</style>