<template>
    <div class="app">
        <h1>你好啊</h1>
        <Person/>
    </div>
</template>

<script>
import Person from './components/Person.vue';
    //js或者ts
    export default{
        name:'APP',  //组件名
        components:{Person}
    }
</script>

<style>
    .app{
        background-color: #ddd;
        box-shadow: 0 0 10px;
        border-radius: 20px;
    }
</style>