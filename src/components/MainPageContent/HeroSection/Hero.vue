<template>
  <v-carousel
  cycle
  hide-delimiter-background
  show-arrows-on-hover
  height="450">
    <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
    >
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  name:"Hero",
  data () {
    return {
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth',
      ],
      items: [
        {
          src: require('../img/HeroSlide2.jpg'),
        },
        {
          src: require('../img/HeroSlide3.jpg'),
        },
        {
          src: require('../img/HeroSlide2.jpg'),
        },
        {
          src: require('../img/HeroSlide3.jpg'),
        },
      ],
    }
  },
}
</script>
