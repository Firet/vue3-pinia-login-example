<script setup>
import { storeToRefs } from 'pinia';

import { useAuthStore } from '@/stores';

const authStore = useAuthStore();
const { user } = storeToRefs(authStore);
</script>

<template>
    <div v-if="user">
        <h1>Bienvenido/a {{user.firstName}}!</h1>
        <p><router-link to="/subsidiaries">Ver Sucursales</router-link></p>
    </div>
</template>
