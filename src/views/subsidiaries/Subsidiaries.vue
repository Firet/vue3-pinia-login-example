<template>
  <div class="card text-center m-3">
    <h5 class="card-header">Sucursales</h5>
    <ul>
      <p>Lista de sucursales disponibles :</p>
      <div v-for="province in filteredSubsidiaries" :key="province.id">
        {{ province.nombre }}
        <!-- : Latitud: {{ province.centroide.lat }}, Longitud:
        {{ province.centroide.lon }} -->
      </div>
    </ul>
  </div>
</template>

<script>
export default {
  name: "get-request",
  data() {
    return {
      filteredSubsidiaries: null,
    };
  },
  created() {
    fetch("https://apis.datos.gob.ar/georef/api/provincias")
      .then((response) => response.json())
      .then(
        (data) =>
          (this.filteredSubsidiaries = data.provincias.filter(
            (province) =>
              province.nombre === "Neuquén" ||
              province.nombre === "Buenos Aires" ||
              province.nombre ===
                "Tierra del Fuego, Antártida e Islas del Atlántico Sur" ||
              province.nombre === "Córdoba" ||
              province.nombre === "Misiones" ||
              province.nombre === "Santa Fe"
          ))
      )
      .catch((error) => {
        this.errorMessage = error;
        console.error("There was an error fetching resources/ Hubo un error consiguiendo recursos", error);
      });
  },
};
</script>
