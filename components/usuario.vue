<template>
  <view>
    <text>Usuario: {{ datosUsuario.username }}</text>
    <text>Nombre: {{ datosUsuario.name }}</text>
    <text>Email: {{ datosUsuario.email }}</text>
    <text>Telefono: {{ datosUsuario.phone }}</text>
    <text>Website: {{ datosUsuario.website }}</text>
  </view>
</template>
<script>
export default {
  props: {
    datosUsuario: Object,
  },
};
</script>

<style>
.usuarioclass {
}
</style>