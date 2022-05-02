<template>
  <div id="app">
    <div class="maincontent">
      <div class="container">
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
      </div>

      <main>
        <transition name="fade" mode="out-in">
          <router-view />
        </transition>
      </main>
    </div>

    <footer :class="`footer footer-${$route.meta.title}`">
      <div class="container">
        <div class="six columns sahaytop">&copy; Sahay</div>
        <div class="six columns right">
          <a href="//arhn.us" target="_blank">Made with 💗 in India</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
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

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5em 0 0em 0;
}

#right a.router-link-exact-active {
  color: #ac8de6;
}

#right a {
  margin-right: 1em;
  font-size: 1.175em;
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
</style>
