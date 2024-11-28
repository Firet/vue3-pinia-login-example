<script setup>
import { useAuthStore } from "@/stores";

const authStore = useAuthStore();
</script>

<template>
  <nav v-show="authStore.user">
    <div class="header">
      <router-link to="/" class="link">
        <img
          class="logo"
          src="/provincia-seguros-imagotipo.jpg"
          alt="Provincia Seguros Logo"
        />
      </router-link>
      <router-link to="/" class="link">
      <div class="header-item">Inicio</div>
      </router-link>
      <router-link to="/subsidiaries" class="link">Nuestras Sucursales</router-link>
      <button @click="authStore.logout()" class="">Cerrar Sesión</button>
    </div>
  </nav>
</template>

<style>
.header {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  background-color: white;
  color: black;
   box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2);
  margin-bottom: 5px;
  width: 100%;
  height: 100px;
}

.logo {
  width: 150px;
  height: 150px;
}

.link {
  color: black;
  text-decoration: none;
}

</style>
