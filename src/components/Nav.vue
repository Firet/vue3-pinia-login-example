<script setup>
import { useAuthStore } from "@/stores";

const authStore = useAuthStore();
</script>

<template>
  <!-- <nav v-show="authStore.user" class="navbar navbar-expand navbar-dark bg-dark"> -->
  <nav v-show="authStore.user">
    <div class="header navbar-nav">
      <router-link to="/" class="link">
        <img
          class="logo"
          src="/provincia-seguros-imagotipo.jpg"
          alt="Provincia Seguros Logo"
        />
      </router-link>

      <div class="header-item">Seguros Personas</div>
      <div>Seguros Empresas</div>
      <div>Proveedores</div>
      <div>Quienes Somos</div>
      <router-link to="/subsidiaries" class="link">Nuestras Sedes</router-link>
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
  border: solid 1px black;
  width: 100%;
  height: 100px;
}

.logo {
  width: 100px;
  height: 100px;
}

.link {
  color: black;
}
</style>
