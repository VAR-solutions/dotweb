<template>
  <v-app>
    <div class="page-container">
      <div class="fullpage-container">
        <div class="fullpage-wp" v-fullpage="opts" ref="example">
          <div class="page-1 page">
            <Home />
          </div>

          <div class="page-2 page">
            <About />
          </div>

          <div class="page-3 page">
            <Projects />
          </div>

          <div class="page-4 page">
             <Team />
          </div>
          <div class="page-5 page">
             <Contact />
          </div>
        </div>
        <button @click="moveNext">next</button>
      </div>
    </div>
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
}

@media screen and (max-width: 700px) {
  .side {
    height: 50%;
  }
}
</style>
