<script setup>
import { storeToRefs } from "pinia";

import { useAuthStore } from "@/stores";

const authStore = useAuthStore();
const { user } = storeToRefs(authStore);
</script>

<template>
  <div class="home-container">
    <div v-if="user">
      <h1>Bienvenido/a {{ user.firstName }}!</h1>
    </div>
  </div>
    <div class="buttons-container">
        <div class="blue-button"><router-link class="blue-link" to="/subsidiaries">Ver Sucursales</router-link></div>
        <div class="blue-button">Cotizá el seguro para tu moto</div>
    </div>

</template>

<style>
.home-container {
    width: 100vw;
    color: black;
}

.buttons-container {
    margin-top: 10rem;
}

.blue-link {
    text-decoration: none;
    color: white;
}

.blue-link:hover {
    text-decoration: none;
    color: white;  
}

.blue-button {
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 20px;
    background-color: mediumblue;
    width: 40%;
    height: 120px;
    margin: 0 auto;
    margin-bottom: 10px;
}

.blue-button:hover {
    background-color: hsl(0, 0%, 15%);
}

@media (max-width: 800px) {
    .blue-button {
        width: 55%;
        font-size: 15px;
    }
}

</style>
