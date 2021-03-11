<template>
  <div>
    <Section1 />
    <Section2 />
  </div>
</template>

<script>
import Section1 from '../components/index/section1'
import Section2 from '../components/index/section2'
export default {
  name: 'index',
  components: {
    Section1,
    Section2,
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

