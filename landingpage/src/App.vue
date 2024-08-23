<template>
  <div>
    <div class="container">
    <HeroSection />
    <SectionTwo />
    <SectionTree />
  </div>
  </div>
</template>


<script>
import SectionTwo from './components/SectionTwo.vue'
import SectionTree from './components/SectionTree.vue'
import HeroSection from './components/HeroSection.vue'

export default {
  name: 'App',
  components: {
    HeroSection,
    SectionTwo,
    SectionTree
  }
}
</script>

<style>
body {
  background-color: #fff;
  display: flex;
  justify-content: center;
  overflow-x: hidden;
}

.container{
  display: flex;
  justify-content: center;
  flex-direction: column;
}


</style>
