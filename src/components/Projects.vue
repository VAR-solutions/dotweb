<template>
  <v-layout row wrap style="height: 100%">
    <v-flex xs12 sm6 md6 lg6 class="d-flex align-center side">
      <v-card elevation="0" max-width="80%" class="mx-auto">
        <h1 class="pb-1 robob lo1" style="color:black; " >
        Our <br>
        Projects
      </h1>
        
        <ul style="list-style-type: none; " class="pl-0 mt-4 robo lo2">
          <li>Poster</li>
          <li>Branding</li>
          <li>Graphics</li>
          <li>Designing</li>
          <li>Illustration</li>
        </ul>
      </v-card>
    </v-flex>

    <v-flex xs12 sm6 md6 lg6 >
      <v-card height="100%" style="background: #404040">
        <v-container grid-list-sm align-content-space-between>
        <v-layout wrap>
          <v-flex>hi</v-flex>
          <v-flex>hello</v-flex>
        </v-layout>
        <v-layout>
          <v-flex>okay</v-flex>
          <v-flex>cool</v-flex>
        </v-layout>
        </v-container>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<style>

.lo1 {
    font-size: 2.8em;
  }
  .lo2 {
    font-size: 1.4em;
  }
@media screen and (max-width: 1000px) {
  .lo1 {
    font-size: 1.0em;
  }
  .lo2 {
    font-size: 0.5em;
  }
}
</style>