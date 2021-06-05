<template>
  <v-carousel
      cycle
      height="600"
      hide-delimiter-background
      show-arrows-on-hover >
    <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
name: `Carousel`,
  data () {
    return {
      items: [

        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
    }
  },
}
</script>

<style scoped>

</style>