<template>
  <div class="text-center">
    <v-btn
        icon
        @click="sheet = !sheet"
    >
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
    <v-bottom-sheet v-model="sheet">
      <v-sheet class="text-center" height="200px">
      <ParallaxHero></ParallaxHero>
      </v-sheet>
    </v-bottom-sheet>
  </div>
</template>

<script>
import ParallaxHero from "@/components/MainPageContent/HeroSection/ParallaxHero";
export default {
name: "SearchBottomNav",
  components:{
  ParallaxHero
  },
  data: () => ({
    sheet: false,
    tiles: [
      { img: 'keep.png', title: 'Keep' },
      { img: 'inbox.png', title: 'Inbox' },
      { img: 'hangouts.png', title: 'Hangouts' },
      { img: 'messenger.png', title: 'Messenger' },
      { img: 'google.png', title: 'Google+' },
    ],
  }),
}
</script>

<style scoped>

</style>