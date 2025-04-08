<template>
    <div class="app">
      <Count/>
      <br>
      <LoveTalk/>
    </div>
  </template>
  
  <script lang="ts" setup name="App">
   import Count from './components/Count.vue';
   import LoveTalk from './components/LoveTalk.vue';
  </script>

<style>
/* App */
body {
    background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
    margin: 0;
    font-family: 'Poppins', sans-serif;
    min-height: 100vh;
}

.app {
    width: 95%;
    max-width: none;
    background-color: rgba(255, 255, 255, 0.9);
    border-radius: 20px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    padding: 40px;
    margin: 20px auto;
    box-sizing: border-box;
}

.title {
    text-align: center;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 600;
    color: #333;
    margin-bottom: 30px;
    background: -webkit-linear-gradient(45deg, #0077b6, #00b4d8);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    letter-spacing: 2px;
}

.navigate {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin-bottom: 40px;
    flex-wrap: wrap;
}

.navigate a {
    text-decoration: none;
    color: #333;
    font-size: clamp(1rem, 2vw, 1.2rem);
    padding: 10px 20px;
    border-radius: 15px;
    transition: all 0.3s ease;
    background-color: rgba(255, 255, 255, 0.5);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
}

.navigate a:hover {
    background-color: #0077b6;
    color: white;
    transform: translateY(-3px);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
}
.navigate a.xiaozhupeiqi {
    background-color: #0077b6;
    color: white;
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
}

.main-content {
    background-color: white;
    border-radius: 15px;
    padding: 30px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
    min-height: 300px;
    line-height: 1.6;
    color: #555;
    font-size: clamp(0.9rem, 2vw, 1rem);
}
</style>