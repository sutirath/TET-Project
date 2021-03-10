<template>
  <div class="bg">
    <div class="container">
      <section class="section">
        <div>
          <img
            src="@/static/images/logo-title.png"
            class="logo-title animed-logotitle"
            alt="title-section1"
          />
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.bg {
  background-image: url('@/static/images/bg.webp');
  background-repeat: no-repeat;
  background-position: top center;
  background-size: cover;
  height: 100vh;
}
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.section {
  min-height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: left;
}

.border-title {
  border: solid 20px rgb(255, 255, 255);
  height: 400px;
  width: 500px;
}

.logo-title {
  width: 600px;
  margin-top: 300px;
  margin-left: -100px;
}

@media screen and (max-width: px) {
  .section {
    min-height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .bg {
    background-image: url('@/static/images/bg.webp');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: cover;
    height: 80 vh;
  }
  .logo-title {
    width: 500px;
    margin-left: -200px;
  }
}

@media screen and (max-width: 1280px) {
  .section {
    min-height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .bg {
    background-image: url('@/static/images/bg.webp');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: cover;
    height: 80 vh;
  }
  .logo-title {
    width: 600px;
    margin-left: -200px;
  }
}

@media screen and (max-width: 1024px) {
  .section {
    min-height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .bg {
    background-image: url('@/static/images/bg.webp');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: cover;
    height: 80 vh;
  }
  .logo-title {
    width: 600px;
    margin-left: -200px;
  }
}

@media screen and (max-width: 1047px) {
  .section {
    min-height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .bg {
    background-image: url('@/static/images/bg.webp');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: cover;
    height: 80 vh;
  }
  .logo-title {
    width: 600px;
    margin-left: -150px;
  }
}

@media screen and (max-width: 768px) {
  .section {
    min-height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .bg {
    background-image: url('@/static/images/bg.webp');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: cover;
    height: 80 vh;
  }
  .logo-title {
    width: 500px;
    margin-left: 0px;
  }
}

@media screen and (max-width: 525px) {
  .section {
    min-height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .bg {
    background-image: url('@/static/images/bg.webp');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: cover;
    height: 80 vh;
  }
  .logo-title {
    width: 350px;
    margin-left: 0px;
  }
}
.animed-logotitle {
  animation: backInDown 2s;
  transition: 0.6s ease all;
}

.logo-title:hover {
  transition: 0.6s ease all;
  width: 650px;
}
</style>

