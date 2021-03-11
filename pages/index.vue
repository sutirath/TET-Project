<template>
  <div>
    <Section1 />
    <Section2 />
    <Section3 />
  </div>
</template>

<script>
import Section1 from '../components/index/section1'
import Section2 from '../components/index/section2'
import Section3 from '../components/index/section3'
export default {
  name: 'index',
  components: {
    Section1,
    Section2,
    Section3,
  },
}
</script>

<style >
@import url('https://fonts.googleapis.com/css2?family=Prompt:wght@300&display=swap');
html,
body {
  font-family: 'Prompt', sans-serif;
}
</style>

