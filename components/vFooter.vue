<template>
  <v-footer
    dark
    padless
    
    id="footer"
  >
 
 
      <v-card-text class="py-2 white--text text-center ">
          <img src="@/assets/SpeedBurguer.png" alt="Logo Speed Burguer">
          <div class="fim">
        Av   Jão da Cunha   nº 99 
       
             Tel:(16)3253-5321
       
        
        </div>
      </v-card-text>
    
  </v-footer>
</template>
<script>
  export default {
    
  }
</script>
<style scoped>
#footer{
  text-shadow: 1px 1px 4px  rgb(251, 253, 232); 
   background-image: linear-gradient(rgb(0, 0, 0), rgb(255, 94, 0));
}
.End{
    letter-spacing: 2px;

}
.fim{
    display: flex;
    justify-content: space-evenly;
    letter-spacing: 2px;
    align-items: center;
}
</style>