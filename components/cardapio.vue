<template>

<div class="black">
<div class="cardapionone">
  <div class="black d-flex text-center" id="alinhar-cardapio">
     <link href="https://fonts.googleapis.com/css?family=Telex&display=swap" rel="stylesheet">
     <div>
     <img class="imgcardapio" src="@/assets/cardapio.jpg" alt="Hamburguers Cardápio">
  </div>
  <div class="white--text">
      <span class="titlecard">CARDÁPIO</span>
      <p><span class="subtitle">Variedade e sabores que agradam a todos os paladares.</span></p>
       <v-btn class="ma-4" outlined color="orange accent-4">CONFIRA AGORA</v-btn>
   </div>
  </div>
  </div>
  <div class="cardapioresponsivo">
      <div class="white--text textocardapio">
      <span class="titlecard">CARDÁPIO</span>
      <p><span class="subtitle">Variedade e sabores que agradam a todos os paladares.</span></p>
       <v-btn class="ma-4" outlined color="orange accent-4">CONFIRA AGORA</v-btn>
   </div>
  <img class="imagemresponsiva" src="@/assets/cardapio.jpg" alt="">
  </div>
  </div>  
 
</template>

<script>
export default {

}
</script>

<style>
*{
    font-family: 'Telex', sans-serif;
}
.titlecard{
   font-size: 80px;
  text-shadow: 1px 1px 4px  rgb(251, 253, 232); 

}
.subtitle{
   font-size: 25px;
   text-shadow: 1px 1px 4px  rgb(251, 253, 232); 

}
#alinhar-cardapio{
   align-items: center;
}
.cardapioresponsivo{
   display: none;
}
@media (max-width: 1100px){
.cardapionone{
   display: none;
}
.imagemresponsiva{
   width: 100%;
}
.cardapioresponsivo{
   text-align: center; 
   display: block; 
}
.textocardapio{
   position: relative;
   top: 80px;
}
.titlecard{
   font-size: 45px;
}
.subtitle{
   font-size: 20px;
   padding: 0px 10px;
}
}
</style>