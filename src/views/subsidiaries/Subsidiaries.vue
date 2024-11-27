<template>
  <div class="card text-center m-3">
    <h5 class="card-header">Sucursales</h5>
    <div class="card-body">Sucursales disponibles: {{ totalVuePackages }}</div>
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
