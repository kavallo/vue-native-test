<template>
  <scroll-view :content-container-style="{ paddingVertical: 40 }">
    <text class="header">Vue Native contributors</text>

    <!-- <github-user v-for="user in users" :key="user.id" :user="user" /> -->
    <usuario
      v-for="usuario in usuarios"
      :key="usuario.id"
      :datosUsuario="usuario"
    />
  </scroll-view>
</template>

<script>
import GithubUser from "./components/GithubUser.vue";
import Usuario from "./components/usuario.vue";
export default {
  data() {
    return {
      usuarios: [],
    };
  },
  async created() {
    // const url = "https://api.github.com/repos/GeekyAnts/vue-native-core/contributors";
    const url = "https://jsonplaceholder.typicode.com/users";
    this.usuarios = await fetch(url).then((res) => res.json());
  },
  methods: {
    onPressButton: function () {
      alert("Clicked Image");
    },
  },
  components: {
    GithubUser,
    Usuario,
  },
};
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
