<template>
  <footer class="footer">
    <p class="copyright">
      © {{ currentYear }} Provincia Seguros - Todos los derechos reservados
    </p>
    <p class="legal">N° de inscripción en SSN <br>
    0499
    Organismo de control<br>
    www.argentina.gob.ar/ssn<br>
    <br>
    La entidad aseguradora dispone de un servicio de Atención al Asegurado que atenderá las consultas y reclamos que presenten los tomadores de seguros, asegurados, beneficiarios y/o derechohabientes.
    <br>
    El Servicio de Atención al Asegurado está integrado por: <br>
    Responsable: 4346-9999 - int 666 - atencion@seguros.com.ar<br>
    Suplente: 4546-9999 - int 999 - suplente@seguros.com.ar<br>
    <br>
    En caso de que el reclamo no haya sido resuelto o haya sido desestimado, total o parcialmente, o que haya sido denegada su adminisión, podrá comunicarse con la Superintendencia de Seguros de la Nación por teléfono,<br>
    correo electrónico a denuncias@seguro.gob.ar o formularios web a través de www.seguros.gob.ar/seguros.<br>
    <br>
    </p>
  </footer>
</template>

<style>
.footer {
  border-top: 1px solid grey;
  bottom: 0;
  width: 100%;
  font-size: 12px;
}

.copyright {
    margin: 1rem;
}

.legal {
    margin: 0 3rem;
}
</style>

<script>
export default {
  computed: {
    currentYear() {
      return new Date().getFullYear();
    },
  },
};
</script>
