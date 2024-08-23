<template>
  <div>
    <SectionTwo />
    <SectionTree />
  </div>
</template>


<script>
import SectionTwo from './components/SectionTwo.vue'
import SectionTree from './components/SectionTree.vue';

export default {
  name: 'App',
  components: {
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
}
</style>
