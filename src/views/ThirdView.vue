<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";
import Button from "primevue/button";

const router = useRouter();
const code = ref("DOW429");

const openWeb = () => {
  window.open("https://www.dominos.com/", "_blank");
};
const lastPage = () => {
    router.push("/second")
};
</script>

<template>
    <main>
        <Button icon="pi pi-user" class="user-btn" />
        <Button icon="pi pi-home" class="home-btn" @click="router.push('/')" />
        <div class = "code-container">
            <h1>Copy Code:</h1>
            <textarea class="code-box" readonly>{{ code }}</textarea>
            <h1>To use coupons online! </h1>
        </div>
        <div class = "order-container">
            <h1>Click here to go to their online store!</h1>
            <button class = "main-btn" @click="openWeb">Order Online</button>
        </div>
        <Button icon="pi pi-angle-double-left" class="back-btn" @click="lastPage" label="Back" />
    </main>
</template>

<style scoped>
        main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: rgba(187, 187, 187, 0.968);
    }

    .code-container {
        font-size: 24px;
        color: #000;
        text-align: center;
        max-width: 80%;
        margin-top: 130px;
    }

    .order-container {
        margin-top: auto; 
        text-align: center;
        margin-bottom: 500px;
        color: #000;
    }

    .code-box {
    width: 300px;
    height: 75px;
    font-size: 52px;
    text-align: center;
    border: 1px solid black;
    border-radius: 5px;
    background-color: rgb(109, 206, 248);
    margin-bottom: 10px;
    resize: none;
    }
    .main-btn {
        background-color: rgb(23, 191, 23);
        color: black;
        font-size: 200%;
        width: 215px;
        height: 75px;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }

    .back-btn {
        position: absolute;
        bottom: 20px;
        left: 20px;
        width: 120px;
        height: 50px;
        background-color: red;
        color: black;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 1.5rem;
        margin-right: 30px;
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
</style>