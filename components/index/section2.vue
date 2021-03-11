<template>
  <div class="sections2">
    <div class="content-left">
      <p class="title-sec2">welcome</p>
      <div>
        <h1>Takeco Engineering</h1>
        <br />
        <h1>History</h1>
      </div>
      <hr />
      <p class="detail-sec2">
        Since 1993, It has been more than 2 decades that Takeco Engineering
        (Thailand)Co.,Ltd was established and operated the business in Steel
        Industry. We serve ourcustomers by heart not only in supplying the best
        tools, equipment, and machinesinstallation for producing steel
        productions, but also conducting a consultant service.In addition, all
        of our engineers are professional, sophisticated and work
        systematical-ly. Resulted with well-understood about all customer's
        needs. Thereby, all of thesebring us a confidential trust from customers
        all along.
      </p>
      <button type="button" class="btn btn-outline-secondary">Welcome</button>
    </div>

    <div class="content-rigth">
      <div class="imgleft-grid">
        <img
          class="img1-sec2"
          id="test"
          src="@/static/images/sections2-logo.png"
          alt="sections2-logo"
        />
      </div>
      <div class="imgrigth-grid">
        <img
          class="img2-sec2"
          src="@/static/images/sections2-logo2.png"
          alt="sections2-logo"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    handleSCroll(event) {
      let header = document.querySelector('.content-rigth')
      if (
        window.scrollY > 200 &&
        !header.className.includes('img-animetions')
      ) {
        header.classList.add('img-animetions')
      } else if (window.scrollY < 50) {
        header.classList.remove('img-animetions')
      }
    },
  },

  mounted() {
    window.addEventListener('scroll', this.handleSCroll)
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleSCroll)
  },
}
</script>

<style>
.img-animetions {
  animation: slideInUp 1s;
}

.sections2 {
  margin-top: 100px;
  margin-left: 120px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-areas: 'content-left content-rigth';
  align-content: center;
}
.content-rigth {
  display: grid;
  grid-template-columns: auto auto;
  grid-template-areas: 'imgleft-grid' 'imgrigth-grid';
}

.title-sec2 {
  color: #b8b7b7;
  font-size: 20px;
  text-align: left;
  margin-bottom: 30px;
}
.content-left h1 {
  font-weight: bolder;
  line-height: 10px;
}
.content-left hr {
  border-radius: 5px;
  margin-top: 50px;
  width: 100px;
  border: 2px solid #c9b194;
  background-color: #c9b194;
}
.detail-sec2 {
  font-size: 12px;
  margin-right: 100px;
  text-align: left;
}
.content-left button {
  margin-bottom: 180px;
  margin-top: 100px;
}

.content-rigth img {
  transition: 0.4s ease all;
  width: 250px;
  height: 449px;
  border-radius: 10px;
}

.content-rigth img:hover {
  transition: 0.4s ease all;
  width: 260px;
  height: 459px;
  box-shadow: 5px 10px 18px #888888;
}

@media screen and (max-width: 1080px) {
  .sections2 {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas:
      'content-left '
      'content-rigth';
  }
  .content-rigth {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas:
      'imgleft-grid'
      'imgrigth-grid';
  }
  .content-rigth img {
    display: none;
  }
}
@media screen and (max-width: 600px) {
  .content-rigth img {
    display: none;
  }
}
@media screen and (max-width: 500px) {
  .content-rigth img {
    display: none;
  }
  .content-left h1 {
    font-weight: bolder;
    line-height: 40px;
  }
}
</style>
