<template>
  <v-layout row wrap style="height: 100%">
    <v-flex xs12 sm6 md6 lg6 class="d-flex align-center" >
      <v-card elevation="0" max-width="80%" class="mx-auto">
        <h1 class="pb-1 robob siz" style="color:black">
          Design is all about
          <br />Connecting dots.
        </h1>
        <h4 class="pt-0 robob">dot,design club - IIIT Vadodara</h4>
        <v-btn class="mt-2" tile color="#404040" dark @click="movetowork">Our Work</v-btn>
      </v-card>
    </v-flex>
    <v-flex xs12 sm6 md6 lg6>
      <v-img style="height: 100%" aspect-ratio src="../assets/home.jpg"></v-img>
    </v-flex>
  </v-layout>
</template>
<script>
export default {
  data () {
    return {

    }
  },
  methods: {
    movetowork(){
      fullpage_api.moveTo(3);
      
    }
  }
}
</script>

<style>
.siz{
  font-size: 2.8em;
}
.siz1{
  font-size: 1.3em;
}
</style>