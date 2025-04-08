<template>
    <Person />
</template>

<script lang="ts" setup name = "App">
import { reactive } from 'vue';
import Person from './components/Person.vue';

</script>

<style>
.app {
    background-color: #ddd;
    box-shadow: 0 0 10px;
    border-radius: 20px;
}
</style>