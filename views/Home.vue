
<template>
 <div>
   <vMenu/>
   <vParalax/>
   <carousellanches/>
   <vcardapio/>
  <vFooter/>
 </div>
</template>

<script>
import vMenu from '@/components/vMenu.vue'
import vParalax from '@/components/paralax.vue'
import carousellanches from '@/components/carousellanches.vue'
import vcardapio from '@/components/cardapio.vue'
import vFooter from '@/components/vFooter.vue'

export default {
  components: {
  vMenu,
  vParalax,
  carousellanches,
  vcardapio,

  vFooter,

  }
}
</script>
<style scoped>

</style>