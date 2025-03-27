<script setup>
import { useRouter } from "vue-router";
import Button from "primevue/button";

const router = useRouter();

const nextPage = () => {
  router.push("/second");
};
</script>

<template>
    <main>
      <Button icon="pi pi-user" class="user-btn" />
      <Button icon="pi pi-home" class="home-btn" @click="router.push('/')" />
      <div>
        <h1 class="title">Dominoes</h1>
        <i class="pi pi-star-fill"></i>
        <i class="pi pi-star-fill"></i>
        <i class="pi pi-star-fill"></i>
        <i class="pi pi-star-fill"></i>
        <i class="pi pi-star-half-fill"></i>
        <div class = "text-container">
          <h2>XXX Boulevard      |      1.2 mi</h2>
          <h2>Speed: 12 min</h2>
          <i class="pi pi-face-smile"></i>
        </div>
        
        <button class="main-btn"@click="nextPage">Order</button>

      </div>
    </main>
  </template>
  
  <style scoped>
    main {
      background-color: rgba(187, 187, 187, 0.968);
      width: 100vw;
      height: 100vh;
      display: flex;
      align-items: center;
      flex-direction: column;
      justify-content: space-between;
      padding: 60px 0;
    }
    .title {
      font-size: 42px;
      color: black;
      margin-top: 140px;
    }

    .text-container{
      color: black;
    }

    .pi-face-smile{
      font-size: 2rem;
      color: yellow;
      padding: 10px;
    }

    .main-btn {
      background-color: rgb(23, 191, 23);
      color: black;
      font-size: 250%;
      width: 250px;
      height: 100px;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      position: relative;
      top: 300px;
    }

    .home-btn {
    position: absolute;
    top: 20px;
    right: 20px;
    font-size: 6rem; 
    color: blue;
    }

    .user-btn {
        position: absolute;
        top: 20px;
        left: 20px;
        font-size: 6rem; 
        color: blue;
    }
    .pi-star-fill {
      font-size: 2rem;
      color: black;
    }
    .pi-star-half-fill {
      font-size: 2rem;
      color: black;
    }
  </style>