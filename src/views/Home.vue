<template>
  <div>
  <Carousel/>
  <MainPageContent/>
  </div>
</template>

<script>
  import Carousel from "@/components/Carousel";
  import MainPageContent from "@/components/MainPageContent/Content/MainPageContent";

  export default {
    name: 'Home',

    components: {
      MainPageContent,
      Carousel,
    },
  }
</script>
