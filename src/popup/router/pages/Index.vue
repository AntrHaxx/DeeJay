<template>
  <v-container fluid>
    <v-layout text-xs-center wrap>
      <v-flex xs4>
        <v-layout>
          <v-flex> <h3>Track Name</h3> </v-flex>
        </v-layout>
        <v-layout>
          <v-flex xs12> <v-slider :color="color" :thumb-color="thumb_color" thumb-label height="10"></v-slider> </v-flex>
        </v-layout>
        <v-layout>
          <v-flex>
            <v-btn-toggle v-model="toggle_exclusive1" class="mb-3">
              <v-btn flat> <v-icon>skip_previous</v-icon> </v-btn>
              <v-btn flat @click="play(1)">
                <v-icon>{{ play_text1 }}</v-icon>
              </v-btn>
              <v-btn flat> <v-icon>skip_next</v-icon> </v-btn>
            </v-btn-toggle>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs4>
        <v-layout>
          <v-flex> <h3>Crossfade</h3> </v-flex>
        </v-layout>
        <v-layout>
          <v-flex>
            <v-btn-toggle class="mt-2">
              <v-btn flat>Random</v-btn>
              <v-btn flat class="px-4">Loop</v-btn>
            </v-btn-toggle>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs4>
        <v-layout>
          <v-flex> <h3>Track Name</h3> </v-flex>
        </v-layout>
        <v-layout>
          <v-flex xs12> <v-slider :color="track_color" :thumb-color="thumb_color" thumb-label height="10"></v-slider> </v-flex>
        </v-layout>
        <v-layout>
          <v-flex>
            <v-btn-toggle v-model="toggle_exclusive2" class="mb-3">
              <v-btn flat> <v-icon>skip_previous</v-icon> </v-btn>
              <v-btn flat @click="play(2)">
                <v-icon>{{ play_text2 }}</v-icon>
              </v-btn>
              <v-btn flat> <v-icon>skip_next</v-icon> </v-btn>
            </v-btn-toggle>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs4 d-flex>
        <v-card flat tile class="d-flex">
          <v-img src="/images/platine.png" aspect-ratio="1" style="background-color: #303030">
            <v-layout slot="placeholder" fill-height align-center justify-center ma-0> <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular> </v-layout>
          </v-img>
        </v-card>
      </v-flex>
      <v-flex xs4 d-flex> <v-slider v-model="val" :color="color" :thumb-color="thumb_color" :track-color="track_color" thumb-label height="10"></v-slider> </v-flex>
      <v-flex xs4 d-flex>
        <v-card flat tile class="d-flex">
          <v-img src="/images/platine2.png" aspect-ratio="1" style="background-color: #303030">
            <v-layout slot="placeholder" fill-height align-center justify-center ma-0> <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular> </v-layout>
          </v-img>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    toggle_exclusive1: null,
    toggle_exclusive2: null,
    play_text1: 'play_arrow',
    play_text2: 'play_arrow',
    val: 50,
    color: 'light-blue',
    thumb_color: 'grey darken-1',
    track_color: 'red',
  }),
  methods: {
    play(index) {
      if (index === 1) {
        if (this.play_text1 === 'play_arrow') {
          this.play_text1 = 'pause';
        } else {
          this.play_text1 = 'play_arrow';
        }
      } else {
        if (this.play_text2 === 'play_arrow') {
          this.play_text2 = 'pause';
        } else {
          this.play_text2 = 'play_arrow';
        }
      }
    },
  },
};
</script>

<style lang="sass" scoped></style>
