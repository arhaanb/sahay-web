<template>
  <div class="vh">
    <div class="container">
      <div class="six columns home">
        <h1 class="zero semi">Sahay</h1>
        <h5>All in one hospital management.</h5>

        <a class="download" target="_blank" href="/download">
          <button class="cool">Download</button>
        </a>

        <router-link to="/about"> Learn more &rarr; </router-link>
      </div>
      <div class="six columns">
        <br class="anti" /><br class="anti" />
        <div>
          <p class="center">
            <img
              src="@/assets/illustration.svg"
              draggable="false"
              alt="illustration"
              class="illus"
            />
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
.home {
  margin-top: 9em;
}

.vh {
  margin: 4em 0 8em 0;
}

.anti {
  display: none;
}
@media (max-width: 750px) {
  .vh {
    margin: 4em 0;
  }
  .home {
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
  margin-top: 2em;
}
.download {
	margin-right: 1em;
}
</style>
