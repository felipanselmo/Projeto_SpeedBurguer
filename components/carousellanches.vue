<template>
  <div id="app ">
    <v-app id="inspire" class="black">
      <v-container class="black">
        <v-card>
          <v-toolbar color="black" dark height="20px" class="black">
            <v-tabs slot="extension" v-model="tab" background-color="transparent" centered class="black">
              <v-tab>HAMBURGUERS</v-tab>
              <v-tab>MAIS PEDIDOS</v-tab>
              <v-tab>NOVIDADES</v-tab>
            </v-tabs>
          </v-toolbar>
        </v-card>

        <v-tabs-items v-model="tab">
          <v-tab-item>
            <!-- Todos os hamburguers -->

            <v-row class="d-flex justify-center flex-wrap black">
              <v-col cols="8" sm="4" v-for="card in cards" :key="card.tile" class="black">
                <v-card id="vcard black">
                  <div class="d-flex pt-5 orange accent-4">
                    <v-img :alt="card.alt" :src="card.src" outlined tile height="210px"></v-img>
                  </div>

                  <v-card-text id="div-text" class="subtitle-1 text-center orange accent-4 black--text" v-text="card.text"></v-card-text>

                  <div class="orange accent-4 black--text d-flex justify-center ">
                    <h3 class v-text="card.valor"></h3>
                  </div>

                  

                  <div class="d-flex justify-center pb-4 orange accent-4">
                    <v-btn color="black orange--text pr-12 pl-12" :href="card.href">Comprar</v-btn>
                  </div>
                </v-card>
              </v-col>
            </v-row>
          </v-tab-item>

          <v-tab-item>
            <!-- Maispedidos-->
<v-row class="d-flex justify-center flex-wrap black">
              <v-col cols="8" sm="4" v-for="card in maispedidos" :key="card.tile" class="black">
                <v-card id="vcard black">
                  <div class="d-flex pt-5 orange accent-4">
                    <v-img :alt="card.alt" :src="card.src" outlined tile height="210px"></v-img>
                  </div>

                  <v-card-text id="div-text" class="subtitle-1 text-center orange accent-4 black--text" v-text="card.text"></v-card-text>

                  <div class="orange accent-4 black--text d-flex justify-center ">
                    <h3 class v-text="card.valor"></h3>
                  </div>

                  

                  <div class="d-flex justify-center pb-4 orange accent-4">
                    <v-btn color="black orange--text pr-12 pl-12" :href="card.href">Comprar</v-btn>
                  </div>
                </v-card>
              </v-col>
            </v-row>

          </v-tab-item>

          <v-tab-item>
            <!-- novidades -->

            <v-row class="d-flex justify-center flex-wrap black">
              <v-col cols="8" sm="4" v-for="card in novidades" :key="card.tile" class="black">
                <v-card id="vcard black">
                  <div class="d-flex pt-5 orange accent-4">
                    <v-img :alt="card.alt" :src="card.src" outlined tile height="210px"></v-img>
                  </div>

                  <v-card-text id="div-text" class="subtitle-1 text-center orange accent-4 black--text" v-text="card.text"></v-card-text>

                  <div class="orange accent-4 black--text d-flex justify-center ">
                    <h3 class v-text="card.valor"></h3>
                  </div>

                  

                  <div class="d-flex justify-center pb-4 orange accent-4">
                    <v-btn color="black orange--text pr-12 pl-12" :href="card.href">Comprar</v-btn>
                  </div>
                </v-card>
              </v-col>
            </v-row>

          </v-tab-item>
        </v-tabs-items>
      </v-container>
    </v-app>
  </div>
 
</template>

<script>
export default {
  data: () => ({
    tab: null,
    cards: [
      {
        marca: "maispedidos",
        text: "Hamburguer",
        valor: "R$22,90",
        
        src: require("@/assets/novidade1.png"),
        alt: "Hamburguer"
      },
      {
        marca: "maispedidos",
        text: "Hamburguer",
        valor: "R$29,99",
       
        src: require("@/assets/novidade1.png"),
        alt: "Hamburguer"
      },
      {
        marca: "novidades",
        text: "Hamburguer",
        valor: "R$25,99",
        
        src: require("@/assets/novidade1.png"),
        alt: "Hamburguer"
      },
      {
        marca: "novidades",
        text: "Hamburguer",
        valor: "R$39,99",
        
        alt: "Hamburguer",
        src: require("@/assets/novidade1.png")
      },
      {
        marca: "maispedidos",
        text: "Hamburguer",
        valor: "R$19,99",
        
        alt: "Hamburguer",
        src: require("@/assets/novidade1.png")
      },
      {
        marca: "novidades",
        text: "Hamburguer",
        valor: "R$29,90",
     
        src: require("@/assets/novidade1.png"),
        alt: "Hamburguer"
      }
    ]
  }),
  computed: {
    maispedidos() {
      return this.cards.filter(p => p.marca == "maispedidos");
    },
    novidades() {
      return this.cards.filter(p => p.marca == "novidades");
    }
  }
};
</script>

<style>

</style>