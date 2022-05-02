<template>
  <div id="app">
    <div class="maincontent">
      <!-- <div class="container">
        <div class="nav">
          <div>
            <router-link class="zero" to="/">
              <img class="logo" draggable="false" src="./assets/logo.svg" alt />
            </router-link>
          </div>
          <div id="right">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
            <a href="/design" target="_blank">Branding</a>
            <a href="/download" target="_blank">Download</a>
          </div>
        </div>
      </div> -->

      <nav class="navbar">
        <div class="navcont">
          <router-link to="/">
            <img draggable="false" class="logo" src="/logo.png" alt="logo" />
          </router-link>

          <div class="links">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
            <a href="/design" target="_blank">Branding</a>
            <a href="/download" target="_blank">Download</a>
          </div>

          <div class="ham" @click="nav = !nav">
            <img src="./assets/ham.svg" alt="Open navbar" />
          </div>
        </div>
      </nav>

      <transition class="nav" name="nav">
        <div v-if="nav" class="fullnav">
          <div class="navcont">
            <div class="topsec">
              <h1>&nbsp;</h1>

              <div class="ham" @click="nav = !nav">
                <img src="./assets/close.svg" alt="Close navbar" />
              </div>
            </div>

            <div class="navdata">
              <div class="flexer">
                <router-link to="/" @click="nav = !nav">Home</router-link>
                <router-link @click="nav = !nav" to="/about">About</router-link>
                <a @click="nav = !nav" href="/design" target="_blank"
                  >Branding</a
                >
                <a @click="nav = !nav" href="/download" target="_blank"
                  >Download</a
                >
              </div>
            </div>
          </div>
        </div>
      </transition>

      <!-- end of nav -->

      <main>
        <transition name="fade" mode="out-in">
          <router-view />
        </transition>
      </main>
    </div>

    <footer :class="`footer footer-${$route.meta.title}`">
      <div class="cont">
        <div class="six columns sahaytop">&copy; Sahay</div>
        <div class="six columns right">
          <a href="//arhn.us" target="_blank">Made with 💗 in India</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nav: false,
    };
  },
  watch: {
    nav() {
      document.querySelector("body").style.overflow = this.nav
        ? "hidden"
        : "auto";
    },
  },
};
</script>

<style scoped lang="scss">
#app {
  position: relative;
  min-height: 97vh;
}

.maincontent {
  padding-bottom: 2em; /* Footer height */
}

footer.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  padding: 1em 0;
  height: 2em; /* Footer height */
}
.logo {
  width: 2.25em;
}

.right {
  text-align: right;
}

@media (max-width: 750px) {
  .logo {
    width: 2em;
  }
  .sahaytop {
    margin-bottom: 0.2em;
  }
}
@media (max-width: 550px) {
  footer.footer {
    text-align: center;
  }
  .right {
    text-align: center;
  }
  #app {
    position: relative;
    min-height: 80vh;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.footer.footer-About {
  padding: 1em 0 !important;
}

/* pooppooo */

.navbar .navcont,
.navcont .topsec {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.navcont .topsec {
  margin-top: 1.45em;
  padding: 0 0.5em;
}
.nav a {
  margin-left: 0.5em;
}
.navbar .links {
  display: flex;
}
.navbar .links a {
  margin-left: 1.75em;
  font-size: 1.15em;
  transition: 0.2s;
}
.navbar .links a.router-link-exact-active {
  color: #ac8de6;
  // color: rgb(60, 124, 233);
}
.navbar .links a:hover {
  color: #ac8de6;
  // color: rgb(60, 124, 233);
}
.navbar {
  padding: 2em 0 1em 0;
  margin-bottom: 1.5em;
}
.nav-enter-active,
.nav-leave-active {
  transition: opacity 0.2s ease;
}
.nav-enter-from,
.nav-leave-to {
  opacity: 0;
}
.ham {
  display: none !important;
}
.ham img {
  width: 1.3em;
}

.fullnav {
  width: 100%;
  height: 100vh;
  background-color: #fff;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 20;
  overflow: hidden;
}

.navdata {
  .flexer {
    display: flex;
    flex-direction: column;
    position: relative;
    margin-top: 3em;
  }
  .btm {
    position: absolute;
    bottom: 5em;
  }
  a {
    font-size: 2em;
    margin-bottom: 0.65em;
    span {
      width: 100% !important;
    }
  }
  a.router-link-exact-active {
    color: #ac8de6;
  }
}

@media (max-width: 750px) {
  .navbar .links {
    display: none;
  }
  .ham {
    display: block !important;
  }
}
</style>
