<template>
  <q-page class="flex flex-center">
    <!-- <h2>Portifólio</h2> -->
    <h2>{{ projects[index] }}</h2>
    <q-btn icon="autorenew" label="Roleta" stack glossy color="red" @click="randomPosition"/>
  </q-page>
</template>

<script>
export default {
  name: 'ProjectsRollet',
  data(){
    return{
      projects: [
        "Sistema de Login",
        "API jogadores",
        "SPA de perfil",
        "API livros",
        "MemeBook"
      ],
      index: 0,
    };
  },
  methods: {
    randomPosition(){
      let index = parseInt(Math.random() * 5 + 0);
      console.log(index);
      this.index = index;
    }
  },
  beforeMount(){
    this.randomPosition();
  }
}
</script>
