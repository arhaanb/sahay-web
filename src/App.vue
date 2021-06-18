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

    <div class="container">
      <footer class="footer">
        <div class="six columns">&copy; Sahay</div>
        <div class="six columns right">
          <a href="//madewithlove.org.in">Made with 💗 in India</a>
        </div>
      </footer>
    </div>
  </div>
</template>

<style scoped>
.logo {
  width: 3.5em;
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
</style>
