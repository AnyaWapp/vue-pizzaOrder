<script setup>
import { useRouter } from "vue-router";
import Button from "primevue/button";

const router = useRouter();

const nextPage = () => {
  router.push("/third");
};
const lastPage = () => {
    router.push("/")
}
</script>

<template>
    <main>
        <Button icon="pi pi-user" class="user-btn" />
        <Button icon="pi pi-home" class="home-btn" @click="router.push('/')" />
        <div class="text-container">
            <h1>
                Click an option to order either online or in-store (in-store unavailable at this time)!
            </h1>
        </div>
            <div class="button-container">
                <button class="main-btn" @click="nextPage">Online</button>
            </div>
            <Button icon="pi pi-angle-double-left" class="back-btn" @click="lastPage" label="Back" />
            <button class="store-btn">In-Store</button>
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

    .text-container {
        text-align: center;
        font-size: 20px;
        color: black;
        max-width: 65%;
        margin-top: 130px;
    }

    .button-container {
        margin-top: auto; 
        margin-bottom: 500px;
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
    }
    
    .store-btn {
      background-color: rgb(115, 234, 115);
      color: black;
      font-size: 250%;
      width: 250px;
      height: 100px;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      position: relative;
      top: -400px;
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