<template>
  <div class="container">
    <section id="home">
      <div class="row">
        <div class="five columns topinfo">
          <h1 class="zero semi">Sahay</h1>
          <h5>A collaborative experience for hospitals to manage resources.</h5>

          <div class="flex-btn">
            <a class="download" target="_blank" href="/download">
              <button class="cool">Download</button>
            </a>
            <router-link class="learn" to="/about"
              >Learn more &rarr;</router-link
            >
          </div>
        </div>
        <div class="seven columns">
          <br class="anti" /><br class="anti" />
          <div>
            <img
              src="/landing.svg"
              draggable="false"
              alt="illustration"
              class="illus u-pull-right"
            />
            <div class="u-cf"></div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
.topinfo {
  margin-top: 8em;
}

#home {
  margin: 4em 0 8.5em 0;
}

.flex-btn {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.learn {
  margin-top: -1.3em;
}

.anti {
  display: none;
}
@media (max-width: 750px) {
  #home {
    margin: 3em 0 7em 0;
  }
  .topinfo {
    margin: 0;
  }
  .anti {
    display: block;
  }
}
p.center {
  text-align: center;
  margin: 0;
}
.illus {
  margin-top: 0em;
  width: 100% !important;
}
.download {
  margin-right: 1em;
}
</style>
