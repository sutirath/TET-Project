<template>
  <nav class="navbar navbar-expand-lg fixed-top navbar-dark text-white">
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarToggler"
      aria-controls="navbarToggler"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <a href="/" class="navbar-brand animate__animated animate__bounce"
      ><img src="@/static/icon.png" height="65" alt="" srcset=""
    /></a>
    <div class="collapse navbar-collapse" id="navbarToggler">
      <dir class="navbar-nav mr-auto name-logo">
        <h4>TAKECO ENGINEERING</h4>
        <p>THAILAND CO.,LTD.</p>
      </dir>

      <dir class="ml-auto">
        <center>
          <h6>{{ $t('Contactus') }} (+66) 344 951 06-8</h6>
        </center>
      </dir>

      <div class="nav navbar-nav navbar-right">
        <a href="" class="btn-circle-facebook .col-sm-6">
          <i class="fab fa-facebook fa-2x"></i
        ></a>

        <a href="" class="btn-circle-youtube .col-sm-6"
          ><i class="fab fa-youtube fa-2x"></i
        ></a>

        <a href="" class="btn-circle-line ..col-sm-6">
          <i class="fab fa-line fa-2x"></i
        ></a>

        <a v-b-toggle.sidebar-right class="btn-circle">
          <i class="fas fa-bars fa-2x"></i
        ></a>

        <!-- <b-button v-b-toggle.sidebar-right
          ><i class="fas fa-bars fa-2x"></i
        ></b-button> -->
        <b-sidebar id="sidebar-right" right backdrop shadow>
          <template #footer="{ hide }">
            <div class="d-flex bg-dark text-light align-items-center px-3 py-2">
              <strong class="mr-auto">TAKECO ENGINEERING</strong>
              <b-button size="sm" @click="hide"
                >{{ $t('navbar-footer') }}
              </b-button>
            </div>
          </template>
          <div class="px-3 py-2">
            <center><h4 id="sidebar-no-header-title">Menu</h4></center>

            <p>
              Cras mattis consectetur purus sit amet fermentum. Cras justo odio,
              dapibus ac facilisis in, egestas eget quam. Morbi leo risus, porta
              ac consectetur ac, vestibulum at eros.
            </p>
            <b-img
              src="https://picsum.photos/500/500/?image=54"
              fluid
              thumbnail
            ></b-img>
            <nuxt-link v-if="$i18n.locale !== 'en'" :to="switchLocalePath('en')"
              >English</nuxt-link
            >
            <nuxt-link v-if="$i18n.locale !== 'th'" :to="switchLocalePath('th')"
              >ไทย</nuxt-link
            >
          </div>
        </b-sidebar>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    handleSCroll(event) {
      let header = document.querySelector('.navbar')
      if (
        window.scrollY > 300 &&
        !header.className.includes('navbae-scrolled')
      ) {
        header.classList.add('navbae-scrolled')
      } else if (window.scrollY < 50) {
        header.classList.remove('navbae-scrolled')
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
.navbar {
  transition: 1s ease all;
}
.navbae-scrolled {
  transition: 2s ease all;
  transition-delay: 10ms;
  background: rgb(87, 87, 87);
  animation: fadeInDown 0.4s;
}
@media screen and (max-width: 768px) {
  .navbar {
    transition: 0.6s ease all;
    transition-delay: 10ms;
    background: rgb(87, 87, 87);
  }
}
.btn-circle,
.btn-circle-facebook,
.btn-circle-youtube,
.btn-circle-line {
  width: 50px;
  height: 30px;
  text-align: center;
  margin: 20px;
  color: rgb(255, 255, 255);
}
.dropdown-menu {
  display: block;
  visibility: hidden;
  opacity: 0;
  transform: translateY(50px);
  transition: 0.5s ease all;
}
.dropdown-menu.show {
  display: block;
  visibility: visible;
  opacity: 1;
  transform: translateY(0px);
  transition: 0.5s ease all;
}
.dropdown:hover .dropdown-menu {
  display: block;
  margin-top: 0;
}

.btn-circle-facebook :hover {
  transform: translate(0px, -10px);
  transition: 0.5s ease all;
  cursor: pointer;
  color: rgb(34, 38, 253);
}
.btn-circle-youtube :hover {
  transform: translate(0px, -10px);
  transition: 0.5s ease all;
  cursor: pointer;
  color: rgb(253, 34, 34);
}
.btn-circle-line :hover {
  transform: translate(0px, -10px);
  transition: 0.5s ease all;
  cursor: pointer;
  color: rgb(35, 207, 19);
}
.dropdow-appbar {
  margin: 20px;
}

.btn-circle.btn-lg {
  width: 50px;
  height: 50px;
  padding: 10px 16px;
  font-size: 18px;
  line-height: 1.33;
  border-radius: 25px;
}
.btn-circle:hover {
  color: white;
  cursor: pointer;
}

.name-logo {
  display: grid;
  line-height: 3px;
}
.name-logo p {
  font-size: 22px;
}

.navbar-brand {
  margin-left: 100px;
}
</style>
