<template>
<div>
  <b-navbar toggleable type="dark" variant="dark">
    <b-navbar-brand href="#">MI APP</b-navbar-brand>
    <div class="links">
    <b-nav-item href="#2">Inicio</b-nav-item>
    <b-nav-item href="#2">Buscar</b-nav-item>
    <b-nav-item href="#2">Acerca de</b-nav-item>
    </div>
        <b-navbar-toggle target="navbar-toggle-collapse">
      <b-navbar-nav>
        <b-nav-item href="#">Link</b-nav-item>
        <b-nav-item href="#" disabled>Disabled</b-nav-item>
      </b-navbar-nav>
      <template #default="{ expanded }">
        <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
        <b-icon v-else icon="chevron-bar-down"></b-icon>
      </template>
    </b-navbar-toggle>

    <b-collapse id="navbar-toggle-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#">Link 1</b-nav-item>
        <b-nav-item href="#">Link 2</b-nav-item>
        <b-nav-item href="#" disabled>Disabled</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>

  <b-container class="my-5 bv-example-row">
    <b-card-group>
    <b-row>
      <b-col class="mb-3" cols="6" sm="8" md="4" lg="4" xl="4" v-for="(personajes,index) in personajes" :key="index">
          <b-card>
            <img :src="personajes.imagen" img-alt="Card image" img-top>
            <b-card-text>
              {{personajes.nombre}}
            </b-card-text>
          </b-card>
      </b-col>
    </b-row>
    </b-card-group>
  </b-container>
</div>
  
</template>

<script>  
export default {
  name: 'Layout',
    data(){
      return {
        personajes: [
          {
          'id' : 1 ,
          'nombre' : 'Morty' ,
          'imagen' :
          'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
          },
          {
          'id' : 2 ,
          'nombre' : 'Rick' ,
          'imagen' :
          'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
          },
          {
          'id' : 3 ,
          'nombre' : 'Summer' ,
          'imagen' :
          'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
          },
          {
          'id' : 4 ,
          'nombre' : 'Beth' ,
          'imagen' :
          'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
          },
          {
          'id' : 5 ,
          'nombre' : 'Jerry' ,
          'imagen' :
          'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
          }
          ]
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.links {
  list-style: none;
  display: flex;
  margin-left: 1000px;
}
.nav-link {
  color: white;
}
</style>
