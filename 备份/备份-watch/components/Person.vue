<template>



</template>

<script lang="ts" setup>
import { type PersonInter } from '@/types'

let person: PersonInter = { id: '001', name: '张三', age: 60 }

let personList: Array<PersonInter> = [
    { id: '001', name: '张三', age: 60 },
    { id: '002', name: '李四', age: 18 },
    { id: '003', name: '王五', age: 5 }
]

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

li {
    font-size: 20px;
}
</style>