<template>
    <div class="person">
       姓：<input type="text"v-model="lastname"><br>
       名：<input type="text"v-model="firstname"><br>
       全名：<span>{{ fullname }}</span><br>
       <button @click="changFullName">将名字改为li-si</button>
    </div>
    
</template>

<script lang="ts" setup>
import { ref,reactive,computed} from 'vue';
   let lastname = ref('张')
   let firstname = ref('三')
   //这么定义的fullname属性是一个计算属性的，且是只读的
//    let fullname = computed(()=>{
//     return lastname.value.slice(0,1).toUpperCase()+lastname.value.slice(1)+'-'+firstname.value;
//    })
    //可读可写
   let fullname = computed({
    get(){
        return lastname.value.slice(0,1).toUpperCase()+lastname.value.slice(1)+'-'+firstname.value;
    },
    set(val){
        const [str1,str2] = val.split('-')
        lastname.value = str1
        firstname.value = str2
        console.log('set',val)
    }
   })

   function changFullName(){

    fullname.value = 'li-si'
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