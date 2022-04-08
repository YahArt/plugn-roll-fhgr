<template>
  <nav class="uk-navbar-container uk-padding-small" uk-navbar>
    <div class="uk-navbar-left">
      <div class="uk-logo">
        <img
          @click="navigateToHome"
          id="logo"
          src="../assets/images/logo.png"
          alt="Plug and Roll Logo"
        />
      </div>
    </div>

    <div class="uk-navbar-center">
      <ul class="uk-navbar-nav">
        <li class="uk-active">
          <a href="#">Geschäftskunden</a>
          <div class="uk-navbar-dropdown">
            <ul class="uk-nav uk-navbar-dropdown-nav">
              <router-link
                to="/property"
                custom
                v-slot="{ navigate, href, route }"
              >
                <li>
                  <a :href="href" @click="navigate">{{ route.name }}</a>
                </li>
              </router-link>
              <router-link
                to="/employer"
                custom
                v-slot="{ navigate, href, route }"
              >
                <li>
                  <a :href="href" @click="navigate">{{ route.name }}</a>
                </li>
              </router-link>
              <router-link
                to="/public_charging"
                custom
                v-slot="{ navigate, href, route }"
              >
                <li>
                  <a :href="href" @click="navigate">{{ route.name }}</a>
                </li>
              </router-link>
              <router-link
                to="/tourism_and_gastro"
                custom
                v-slot="{ navigate, href, route }"
              >
                <li>
                  <a :href="href" @click="navigate">{{ route.name }}</a>
                </li>
              </router-link>
              <li><a href="#">Referenzen</a></li>
            </ul>
          </div>
        </li>
        <li>
          <a href="#">Produkte & Dienstleistungen</a>
          <div class="uk-navbar-dropdown">
            <ul class="uk-nav uk-navbar-dropdown-nav">
              <li><a href="#">Ladestationen</a></li>
              <li><a href="#">Installationen</a></li>
              <li><a href="#">Lastmanagement</a></li>
              <li><a href="#">Servicepakete</a></li>
              <li><a href="#">Software</a></li>
              <li><a href="#">Garagenprüfung</a></li>
            </ul>
          </div>
        </li>
        <li>
          <a href="#">E-Auto Fahrer</a>
          <div class="uk-navbar-dropdown">
            <ul class="uk-nav uk-navbar-dropdown-nav">
              <li><a href="#">Netzwerk</a></li>
              <li><a href="#">Ladeanleitung</a></li>
              <li><a href="#">Zuhause laden</a></li>
              <li><a href="#">Produkte & Shop</a></li>
            </ul>
          </div>
        </li>
        <li>
          <a href="#">Partner</a>
        </li>
        <li>
          <a href="#">Über Uns</a>
          <div class="uk-navbar-dropdown">
            <ul class="uk-nav uk-navbar-dropdown-nav">
              <li><a href="#">Team</a></li>
              <li><a href="#">Webinar & Events</a></li>
              <li><a href="#">Support</a></li>
              <li><a href="#">Blog</a></li>
              <li><a href="#">Newsletter</a></li>
            </ul>
          </div>
        </li>
      </ul>
    </div>

    <div class="uk-navbar-right">
      <ul class="uk-navbar-nav">
        <li>
          <a href="#">Login</a>
        </li>
        <li>
          <a href="#">Registrieren</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Header",
  props: {},
  components: {},
  methods: {
    navigateToHome: function () {
      this.$router.push("/");
    },
  },
};
</script>

<style scoped>
.uk-navbar-container {
  background-color: #3d3c3c;
}

li.uk-active > a {
  color: rgb(168, 173, 0);
}

#logo {
  max-height: 60px;
  cursor: pointer;
}
</style>
