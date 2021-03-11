<template>
  <div class="section3-bg">
    <div class="container-section3">
      <div class="section3-left"></div>
      <div class="section3-rigth">
        <p class="title1-section3">{{ $t('section3.title1') }}</p>
        <h1 class="title2-section3">{{ $t('section3.title2') }}</h1>
        <p>{{ $t('section3.detail') }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.section3-bg {
  background-image: url('@/static/images/section3-bg.png');
  background-repeat: no-repeat;
  background-position: top center;
  background-size: cover;
  height: 100vh;
}
.container-section3 {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-areas: 'section3-left section3-rigth';
}
.section3-rigth {
  margin-top: 200px;
  margin-right: 200px;
}
.title1-section3 {
  font-size: 30px;
  color: #bd8929;
  -webkit-text-stroke: 0.2px black;
}
.title2-section3 {
  font-weight: bolder;
  color: #bd8929;
}
</style>
