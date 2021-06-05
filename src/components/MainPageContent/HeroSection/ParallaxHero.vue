<template>
  <div>
    <v-parallax height="300" dark src="../img/ParallaxImage.jpg">
      <v-container fluid grid-list-xl>
        <v-layout justify-center row wrap>
          <v-flex xs12 style="text-align: center;">
            <h4 class=" blue--text font-weight-thin mb-9 ">Find what you desire</h4>
            <v-flex xs12>
              <v-layout align-center justify-center row wrap>
                <v-flex xs6>
                  <v-layout>
                    <v-text-field
                        outlined
                        label="search"
                        append-icon="mdi-magnify"
                        rounded
                    ></v-text-field>
                  </v-layout>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-flex>
          <v-row xs6  justify="space-around">
            <v-col cols="5" sm="2" md="8">
              <v-chip-group multiple active-class="primary--text">
                <v-chip v-for="tag in tags" :key="tag">
                  {{ tag }}
                </v-chip>
              </v-chip-group>
            </v-col>
          </v-row>
        </v-layout>
      </v-container>
    </v-parallax>
  </div>
</template>

<script>
export default {
name: "ParallaxHero.vue",
  data: () => ({
    tags: [
      "Work",
      "Home Improvement",
      "Vacation",
      "Food",
      "Drawers",
      "Shopping",
      "Art",
      "Tech",
      "Creative Writing"
    ]
  })
}
</script>

<style scoped>

</style>