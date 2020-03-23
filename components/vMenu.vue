
<template>
<header>
  <div class="topo">
    <link href="https://fonts.googleapis.com/css?family=Telex&display=swap" rel="stylesheet">

    <div class="Burguer">
    <v-app-bar-nav-icon  color="orange accent-4" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>  
    
     <v-navigation-drawer
      v-model="drawer "
      absolute
      temporary
      dark
      class="transparent"
      width="180"
      
    >
      <v-list
        nav
        dense
        
        
      >
        <v-list-item-group
          v-model="group"
          active-class=" text--accent-4"
          class="pt-8"
          
        
        >
          <v-list-item  class="orange--text">
            <v-list-item-title>Pedido online</v-list-item-title>
          </v-list-item>

          <v-list-item  class="orange--text">
            <v-list-item-title>Cardápio</v-list-item-title>
          </v-list-item>

          <v-list-item class="orange--text">
            <v-list-item-title>Acompanhe seu pedido</v-list-item-title>
          </v-list-item>

          <v-list-item  class="orange--text">
            <v-list-item-title>Cadastrar</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

   </div>
    <div class="logo">
   <img src="@/assets/SpeedBurguer.png" alt="Logo Speed Burguer">
   </div>
   <nav>
     <a class="pa-5  white--text" href=""> Pedido online</a>
     <a class="pa-5 white--text"  href="">Cardápio</a>
     <a class="pa-5 white--text"  href="">Acompanhe seu pedido</a>
     <a class="pa-5  white--text"  href="">Cadastrar</a>
   </nav>
   <div>
     <v-btn icon >
        <v-icon color="orange accent-4">mdi-shopping</v-icon>
      </v-btn>

       <v-btn icon >
        <v-icon color="orange accent-4">mdi-account-circle</v-icon>
      </v-btn>
      </div>
  </div>
  </header>
</template>

<script>
  export default {
    data: () => ({
      drawer: false,
      group: null,
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>

<style scoped>
.topo{
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #000000;
}
.Burguer{
  display: none;
}
a{
text-decoration: none;
}
nav a:hover{
text-shadow: 1px 1px 4px  rgb(251, 253, 232); 
}
nav a{
  font-weight: bold;
  text-align: center;
  font-family: 'Telex', sans-serif;
  letter-spacing: 2px;
}
nav{
  border-radius: 5px;
}
@media (max-width: 855px){
  .topo{
    justify-content: space-around;
  }
.Burguer{
  display: block;
}
nav{
  display: none;
}


}
</style>