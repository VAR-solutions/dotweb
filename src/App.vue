<template>
  <v-app>
    <full-page ref="fullpage" :options="options" id="fullpage">
    <div class="section">
      <!-- <button class="next" @click="$refs.fullpage.api.moveSectionDown()">Next</button> -->
      <Home />
    </div>
    <div class="section">
      <!-- <button class="prev" @click="$refs.fullpage.api.moveSectionUp()">Prev</button> -->
      <About />
    </div>
     <div class="section">
      <!-- <button class="prev" @click="$refs.fullpage.api.moveSectionUp()">Prev</button> -->
      <Projects />
    </div>
     <div class="section">
      <!-- <button class="prev" @click="$refs.fullpage.api.moveSectionUp()">Prev</button> -->
      <Team />
    </div>
    <div class="section">
      <!-- <button class="prev" @click="$refs.fullpage.api.moveSectionUp()">Prev</button> -->
      <Contact />
    </div>
  </full-page>
  </v-app>
</template>

<script>
import Home from '../src/components/Home';
import About from '../src/components/About';
import Projects from '../src/components/Projects';
import Team from '../src/components/Team';
import Contact from '../src/components/Contact';
export default {
  name: "App",
  components: {
    Home,
    About,
    Projects,
    Team,
    Contact

  },
  data() {
    return {
      opts: {
        start: 0,
        dir: "v",
        duration: 500,
        beforeChange: function(currentSlideEl, currenIndex, nextIndex) {},
        afterChange: function(currentSlideEl, currenIndex, nextIndex) {}
      }
    };
  },
  method: {
    moveNext() {
      this.$refs.example.$fullpage.moveNext(); //Move to the next page
    }
  }
};
</script>



<style>
.page-container {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
}
.page-1 {
  background: white;
  color: #404040;
}
.page-2 {
  background: white;
  color: #404040;
}
.page-3 {
  background: white;
  color: #404040;
}
.side {
  height: 100%;
  background-color: white;
}

@media screen and (max-width: 700px) {
  .side {
    height: 50%;
  }
}


</style>
