<template>
  <div id="app">
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
        </div>
      </div>
    </div>

    <main>
      <transition name="fade" mode="out-in">
        <router-view />
      </transition>
    </main>

    <footer :class="`footer footer-${$route.meta.title}`">
      <div class="container">
        <div class="six columns sahaytop">&copy; Sahay</div>
        <div class="six columns right">
          <a href="//madewithlove.org.in" target="_blank">Made with 💗 in India</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.logo {
  width: 2.5em;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.75em 0;
}

#right a.router-link-exact-active {
  color: #ac8de6;
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
