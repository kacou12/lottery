<template>
  <div>
    <div class="row col-md-8 mx-auto">
      <pack v-for="(item, n) in items" :key="n" :pack="item"></pack>
    </div>
  </div>
</template>

<script>
import pack from '@/components/pack.vue'
import Vue from 'vue'
export default Vue.extend({
  components: { pack },
  data() {
    return {
      items: [
        {
          title: 'Silver Pack',
          rating: 3,
          mise: 450,
          gain: 250000,
          participant: 140,
          description:
            'Le meilleur a la mesure de vos attentes , essayez et vous verez',
          horaire: '14H30',
          image: '/crypto-currency.jpg',
          height: 150,
        },
        {
          title: 'Gold Pack',
          rating: 5,
          mise: 1500,
          gain: 4500000,
          participant: 310,
          description:
            "Le meilleur des packs lotteries , gaganer jusqu'a 15 mill euros comptabilisé en voyages , cadeau, et plein d'autre chose a decouvrir",
          horaire: '18H30',
          image: '/crypto-currency.jpg',
          height: 250,
        },
        {
          title: 'bronze Pack',
          rating: 2,
          mise: 100,
          gain: 80000,
          participant: 100,
          description:
            "Le meilleur des packs lotteries , gaganer jusqu'a 15 mill euros comptabilisé en voyages , cadeau, et plein d'autre chose a decouvrir",
          horaire: '13H30',
          image: '/crypto-currency.jpg',
          height: 150,
        },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
</style>