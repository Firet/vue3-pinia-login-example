<template>
  <div class="card text-center m-3">
    <h5 class="card-header">Sucursales</h5>
    <ul>
      <p>Lista de sucursales disponibles :</p>
      <li v-for="province in totalVuePackages" :key="province.id">
        {{ province.nombre }}: Latitud: {{ province.centroide.lat }}, Longitud:
        {{ province.centroide.lon }}
      </li>

    </ul>
  </div>
</template>

<script>
export default {
  name: "get-request",
  data() {
    return {
      totalVuePackages: null,
    };
  },
  created() {
    fetch("https://apis.datos.gob.ar/georef/api/provincias")
      .then((response) => response.json())
      .then(
        (data) =>
          (this.totalVuePackages = data.provincias.filter(
            (province) =>
              province.nombre === "Neuquén" ||
              province.nombre === "Buenos Aires" ||
              province.nombre ===
                "Tierra del Fuego, Antártida e Islas del Atlántico Sur" ||
              province.nombre === "Córdoba" ||
              province.nombre === "Misiones" ||
              province.nombre === "Santa Fé"
          ))
      );
  },
};
</script>
